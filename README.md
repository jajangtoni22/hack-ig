# hack-ig
We are anonymus
<div class="container">

    <div class="center-form panel">
      <div class="panel-body">
        <h4 class="text-center"><i class="ion-log-in"></i> Log in</h4>

        <form name="loginForm" ng-submit="emailLogin()" novalidate>
          <div class="form-group has-feedback" ng-class="{ 'has-error': loginForm.email.$invalid && loginForm.email.$dirty }">
            <input server-error class="form-control input-lg" type="text" name="email" ng-model="email" placeholder="Email" required autofocus>
            <span class="ion-at form-control-feedback"></span>
            <div class="help-block" ng-if="loginForm.email.$dirty" ng-messages="loginForm.email.$error">
              <div ng-message="required">Please enter your email</div>
              <div ng-message="server">{{errorMessage.email}}</div>
            </div>
          </div>

          <div class="form-group has-feedback" ng-class="{ 'has-error': loginForm.password.$invalid && loginForm.password.$dirty }">
            <input server-error class="form-control input-lg" type="password" name="password" ng-model="password" placeholder="Password" required>
            <span class="ion-key form-control-feedback"></span>
            <div class="help-block" ng-if="loginForm.password.$dirty" ng-messages="loginForm.password.$error">
              <div ng-message="required">Please enter your password</div>
              <div ng-message="server">{{errorMessage.password}}</div>
            </div>
          </div>

          <button type="submit" class="btn btn-block btn-success" ng-disabled="loginForm.$invalid">Log in</button>

          <br/>

          <p class="text-center text-muted">
            <small>Don't have an account yet? <a href="#/signup">Sign up</a></small>
          </p>

          <div class="signup-or-separator">
            <h6 class="text">or</h6>
            <hr>
          </div>
        </form>
        <button class="btn btn-block btn-instagram" ng-click="instagramLogin()">
          <i class="ion-social-instagram"></i> Sign in with Instagram
        </button>
      </div>
    </div>

</div>
