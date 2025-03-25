<script setup lang="ts">

</script>

<template>
    <div>
        <footer class="footer sm:footer-horizontal bg-[#202020] text-white text-base-content p-10">
            <nav>
                <h6 class="footer-title">Services</h6>
                <a class="link link-hover">Branding</a>
                <a class="link link-hover">Design</a>
                <a class="link link-hover">Marketing</a>
                <a class="link link-hover">Advertisement</a>
            </nav>
            <nav>
                <h6 class="footer-title">Company</h6>
                <a class="link link-hover">About us</a>
                <a class="link link-hover">Contact</a>
                <a class="link link-hover">Jobs</a>
                <a class="link link-hover">Press kit</a>
            </nav>
            <nav>
                <h6 class="footer-title">Legal</h6>
                <a class="link link-hover">Terms of use</a>
                <a class="link link-hover">Privacy policy</a>
                <a class="link link-hover">Cookie policy</a>
            </nav>
            <form>
                <h6 class="footer-title">Newsletter</h6>
                <fieldset class="lg:w-80">
                    <label>Enter your email address</label>
                    <div class="join">
                        <input type="text" placeholder="username@site.com" class="input input-bordered join-item" />
                        <button class="btn btn-primary join-item">Subscribe</button>
                    </div>
                </fieldset>
            </form>
        </footer>
    </div>
</template>

<style scoped></style>