---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273028"
---
# <span data-ttu-id="42290-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="42290-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="42290-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42290-102">SYNOPSIS</span></span>
<span data-ttu-id="42290-103">新增主廚延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="42290-104">句法</span><span class="sxs-lookup"><span data-stu-id="42290-104">SYNTAX</span></span>

### <span data-ttu-id="42290-105">Linux</span><span class="sxs-lookup"><span data-stu-id="42290-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42290-106">時間</span><span class="sxs-lookup"><span data-stu-id="42290-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42290-107">說明</span><span class="sxs-lookup"><span data-stu-id="42290-107">DESCRIPTION</span></span>
<span data-ttu-id="42290-108">**AzVMChefExtension** Cmdlet 會將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="42290-109">示例</span><span class="sxs-lookup"><span data-stu-id="42290-109">EXAMPLES</span></span>

### <span data-ttu-id="42290-110">範例1：新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="42290-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="42290-111">這個命令會將主廚延伸新增到名為 WindowsVM001 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="42290-112">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="42290-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="42290-113">範例2：新增主廚延伸至 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="42290-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="42290-114">這個命令會將主廚延伸新增到名為 LinuxVM001 的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="42290-115">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="42290-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="42290-116">範例3：使用 [引導選項] 新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="42290-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="42290-117">這個命令會將主廚延伸新增到名為 WindowsVM002 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="42290-118">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="42290-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="42290-119">在引導之後，虛擬機器會參照 JSON 格式所指定的 BootstrapOptions。</span><span class="sxs-lookup"><span data-stu-id="42290-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="42290-120">參數</span><span class="sxs-lookup"><span data-stu-id="42290-120">PARAMETERS</span></span>

### <span data-ttu-id="42290-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="42290-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="42290-122">-BootstrapOptions</span></span>
<span data-ttu-id="42290-123">指定 [client_rb] 選項中的 [設定]。</span><span class="sxs-lookup"><span data-stu-id="42290-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="42290-124">-BootstrapVersion</span></span>
<span data-ttu-id="42290-125">指定啟動配置的版本。</span><span class="sxs-lookup"><span data-stu-id="42290-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="42290-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="42290-127">指定主廚服務執行的頻率 (（分鐘）) 。</span><span class="sxs-lookup"><span data-stu-id="42290-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="42290-128">如果您不想要在 Azure VM 上安裝主廚服務，請將此欄位中的值設為0。</span><span class="sxs-lookup"><span data-stu-id="42290-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="42290-129">-ChefServerUrl</span></span>
<span data-ttu-id="42290-130">將主廚伺服器連結指定為 URL。</span><span class="sxs-lookup"><span data-stu-id="42290-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="42290-131">-ClientRb</span></span>
<span data-ttu-id="42290-132">指定主廚用戶端. rb 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="42290-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-133">-守護程式</span><span class="sxs-lookup"><span data-stu-id="42290-133">-Daemon</span></span>
<span data-ttu-id="42290-134">為無人參與的執行設定主廚用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="42290-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="42290-135">節點平臺應該是 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="42290-135">The node platform should be Windows.</span></span>
<span data-ttu-id="42290-136">允許的選項： "none"、"service" 和 "task"。</span><span class="sxs-lookup"><span data-stu-id="42290-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="42290-137">none-目前禁止主廚-用戶端服務被設定為服務。</span><span class="sxs-lookup"><span data-stu-id="42290-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="42290-138">服務-將主廚用戶端設定為在背景中自動執行，成為服務。</span><span class="sxs-lookup"><span data-stu-id="42290-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="42290-139">任務-將主廚用戶端設定為在背景中自動執行，做為排程任務。</span><span class="sxs-lookup"><span data-stu-id="42290-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42290-140">-DefaultProfile</span></span>
<span data-ttu-id="42290-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42290-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="42290-142">-JsonAttribute</span></span>
<span data-ttu-id="42290-143">要新增至第一次執行主廚-用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="42290-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="42290-144">例如，-JsonAttribute "{" foo "：" bar "}"</span><span class="sxs-lookup"><span data-stu-id="42290-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="42290-145">-Linux</span></span>
<span data-ttu-id="42290-146">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-147">-位置</span><span class="sxs-lookup"><span data-stu-id="42290-147">-Location</span></span>
<span data-ttu-id="42290-148">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="42290-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="42290-149">-Name</span></span>
<span data-ttu-id="42290-150">指定主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="42290-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="42290-151">-NoWait</span></span>
<span data-ttu-id="42290-152">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="42290-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="42290-153">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="42290-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="42290-154">-OrganizationName</span></span>
<span data-ttu-id="42290-155">指定主廚延伸的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="42290-155">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42290-156">-ResourceGroupName</span></span>
<span data-ttu-id="42290-157">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42290-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="42290-158">-RunList</span></span>
<span data-ttu-id="42290-159">指定 [主廚] 節點的 [執行] 清單。</span><span class="sxs-lookup"><span data-stu-id="42290-159">Specifies the Chef node run list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-160">密碼</span><span class="sxs-lookup"><span data-stu-id="42290-160">-Secret</span></span>
<span data-ttu-id="42290-161">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="42290-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="42290-162">-SecretFile</span></span>
<span data-ttu-id="42290-163">檔案的路徑，該檔案包含用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="42290-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="42290-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="42290-165">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="42290-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="42290-166">-ValidationClientName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="42290-167">-ValidationPem</span></span>
<span data-ttu-id="42290-168">指定主廚驗證程式. pem 檔路徑</span><span class="sxs-lookup"><span data-stu-id="42290-168">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="42290-169">-VMName</span></span>
<span data-ttu-id="42290-170">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="42290-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="42290-171">這個 Cmdlet 會為此參數指定的虛擬機器新增主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="42290-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42290-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="42290-172">-Windows</span></span>
<span data-ttu-id="42290-173">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="42290-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-174">-確認</span><span class="sxs-lookup"><span data-stu-id="42290-174">-Confirm</span></span>
<span data-ttu-id="42290-175">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42290-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42290-176">-WhatIf</span></span>
<span data-ttu-id="42290-177">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="42290-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42290-178">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="42290-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42290-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42290-179">CommonParameters</span></span>
<span data-ttu-id="42290-180">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42290-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42290-181">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42290-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42290-182">輸入</span><span class="sxs-lookup"><span data-stu-id="42290-182">INPUTS</span></span>

### <span data-ttu-id="42290-183">System.object</span><span class="sxs-lookup"><span data-stu-id="42290-183">System.String</span></span>

### <span data-ttu-id="42290-184">System.object</span><span class="sxs-lookup"><span data-stu-id="42290-184">System.Boolean</span></span>

## <span data-ttu-id="42290-185">輸出</span><span class="sxs-lookup"><span data-stu-id="42290-185">OUTPUTS</span></span>

### <span data-ttu-id="42290-186">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="42290-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="42290-187">筆記</span><span class="sxs-lookup"><span data-stu-id="42290-187">NOTES</span></span>

## <span data-ttu-id="42290-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="42290-188">RELATED LINKS</span></span>

[<span data-ttu-id="42290-189">AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="42290-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="42290-190">移除-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="42290-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
