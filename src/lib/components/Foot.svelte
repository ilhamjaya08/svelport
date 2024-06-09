<script>
    import { Footer, FooterCopyright, FooterLinkGroup, FooterLink, FooterBrand, FooterIcon } from 'flowbite-svelte';
    import Icon from '@iconify/svelte';
  </script>
  
  <Footer footerType="socialmedia" class="border-t-2 border-gray-200 mt-4">
    <div class="md:flex md:justify-between">
      <div class="mb-6 md:mb-0">
        <FooterBrand href="/" src="https://avatars.githubusercontent.com/u/141555404?v=4" alt="Muhammad Ilham Jaya " name="ilhamjaya08" />
      </div>
      <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
        <div>
          <h2 class="mb-6 text-sm font-semibold text-gray-900 uppercase dark:text-white">Contact</h2>
          <FooterLinkGroup>
            <FooterLink liClass="mb-4" href="https://instagram.com/ilham.j_08">Instagram</FooterLink>
            <FooterLink liClass="mb-4" href="t.me/@ilhamjaya08">Telegram</FooterLink>
            <FooterLink liClass="mb-4" href="https://discord.gg/AdgwXdmBqC">Discord</FooterLink>
            <FooterLink liClass="mb-4" href="https://linktr.ee/ilhamjaya08">Others</FooterLink>
          </FooterLinkGroup>
        </div>
        <div>
          <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Page</h2>
          <FooterLinkGroup>
            <FooterLink liClass="mb-4" href="/about">About</FooterLink>
            <FooterLink liClass="mb-4" href="/works">Works</FooterLink>
            <FooterLink liClass="mb-4" href="/contact">Contact</FooterLink>
            <FooterLink liClass="mb-4" href="/resume">Resume/CV</FooterLink>
          </FooterLinkGroup>
        </div>
        <div>
          <h2 class="mb-6 text-sm font-semibold uppercase text-gray-900 dark:text-white">Others</h2>
          <FooterLinkGroup>
            <FooterLink liClass="mb-4" href="https://t.me/@ilhamjaya08">Order an app</FooterLink>
            <FooterLink liClass="mb-4" href="https://t.me/@ilhamjaya08">Hire me</FooterLink>
          </FooterLinkGroup>
        </div>
      </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
    <div class="sm:flex sm:items-center sm:justify-between">
      <FooterCopyright href="/" by="Muhammad Ilham Jaya " />
      <div class="flex mt-4 space-x-6 rtl:space-x-reverse sm:justify-center sm:mt-0">
        <FooterIcon href="/">
          <Icon icon="flowbite:github-solid" class="w-5 h-5 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
        <FooterIcon href="/">
          <Icon icon="flowbite:discord-solid" class="w-5 h-5 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
        <FooterIcon href="/">
          <Icon icon="flowbite:instagram-solid" class="w-5 h-5 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
        <FooterIcon href="/">
          <Icon icon="flowbite:facebook-solid" class="w-5 h-5 text-gray-500 dark:text-gray-500 hover:text-gray-900 dark:hover:text-white" />
        </FooterIcon>
      </div>
    </div>
  </Footer>