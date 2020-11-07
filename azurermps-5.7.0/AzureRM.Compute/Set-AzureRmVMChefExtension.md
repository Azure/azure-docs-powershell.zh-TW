---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMChefExtension.md
ms.openlocfilehash: 25ddfd3fcb7d087db493e87bdd9781b2bbb77040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623605"
---
# <span data-ttu-id="678ba-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="678ba-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="678ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="678ba-102">SYNOPSIS</span></span>
<span data-ttu-id="678ba-103">新增主廚延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="678ba-104">SYNTAX</span></span>

### <span data-ttu-id="678ba-105">Linux</span><span class="sxs-lookup"><span data-stu-id="678ba-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678ba-106">時間</span><span class="sxs-lookup"><span data-stu-id="678ba-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678ba-107">說明</span><span class="sxs-lookup"><span data-stu-id="678ba-107">DESCRIPTION</span></span>
<span data-ttu-id="678ba-108">**AzureVMChefExtension** Cmdlet 會將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="678ba-109">示例</span><span class="sxs-lookup"><span data-stu-id="678ba-109">EXAMPLES</span></span>

### <span data-ttu-id="678ba-110">範例1：新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="678ba-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="678ba-111">這個命令會將主廚延伸新增到名為 WindowsVM001 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="678ba-112">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="678ba-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="678ba-113">範例2：新增主廚延伸至 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="678ba-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="678ba-114">這個命令會將主廚延伸新增到名為 LinuxVM001 的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="678ba-115">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="678ba-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="678ba-116">範例3：使用 [引導選項] 新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="678ba-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="678ba-117">這個命令會將主廚延伸新增到名為 WindowsVM002 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="678ba-118">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="678ba-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="678ba-119">在引導之後，虛擬機器會參照 JSON 格式所指定的 BootstrapOptions。</span><span class="sxs-lookup"><span data-stu-id="678ba-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="678ba-120">參數</span><span class="sxs-lookup"><span data-stu-id="678ba-120">PARAMETERS</span></span>

### <span data-ttu-id="678ba-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="678ba-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="678ba-122">-BootstrapOptions</span></span>
<span data-ttu-id="678ba-123">指定 [client_rb] 選項中的 [設定]。</span><span class="sxs-lookup"><span data-stu-id="678ba-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="678ba-124">-BootstrapVersion</span></span>
<span data-ttu-id="678ba-125">指定啟動配置的版本。</span><span class="sxs-lookup"><span data-stu-id="678ba-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="678ba-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="678ba-127">指定主廚服務執行的頻率 (（分鐘）) 。</span><span class="sxs-lookup"><span data-stu-id="678ba-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="678ba-128">如果您不想要在 Azure VM 上安裝主廚服務，請將此欄位中的值設為0。</span><span class="sxs-lookup"><span data-stu-id="678ba-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="678ba-129">-ChefServerUrl</span></span>
<span data-ttu-id="678ba-130">將主廚伺服器連結指定為 URL。</span><span class="sxs-lookup"><span data-stu-id="678ba-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="678ba-131">-ClientRb</span></span>
<span data-ttu-id="678ba-132">指定主廚用戶端. rb 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="678ba-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-133">-守護程式</span><span class="sxs-lookup"><span data-stu-id="678ba-133">-Daemon</span></span>
<span data-ttu-id="678ba-134">為無人參與的執行設定主廚用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="678ba-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="678ba-135">節點平臺應該是 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="678ba-135">The node platform should be Windows.</span></span>
<span data-ttu-id="678ba-136">允許的選項： "none"、"service" 和 "task"。</span><span class="sxs-lookup"><span data-stu-id="678ba-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="678ba-137">none-目前禁止主廚-用戶端服務被設定為服務。</span><span class="sxs-lookup"><span data-stu-id="678ba-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="678ba-138">服務-將主廚用戶端設定為在背景中自動執行，成為服務。</span><span class="sxs-lookup"><span data-stu-id="678ba-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="678ba-139">任務-將主廚-用戶端自動在背景中做為 secheduled 任務自動執行。</span><span class="sxs-lookup"><span data-stu-id="678ba-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-140">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="678ba-140">-JsonAttribute</span></span>
<span data-ttu-id="678ba-141">要新增至第一次執行主廚-用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="678ba-141">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="678ba-142">例如，-JsonAttribute "{" foo "：" bar "}"</span><span class="sxs-lookup"><span data-stu-id="678ba-142">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-143">-Linux</span><span class="sxs-lookup"><span data-stu-id="678ba-143">-Linux</span></span>
<span data-ttu-id="678ba-144">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-144">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-145">-位置</span><span class="sxs-lookup"><span data-stu-id="678ba-145">-Location</span></span>
<span data-ttu-id="678ba-146">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="678ba-146">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="678ba-147">-Name</span></span>
<span data-ttu-id="678ba-148">指定主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="678ba-148">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-149">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="678ba-149">-OrganizationName</span></span>
<span data-ttu-id="678ba-150">指定主廚延伸的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="678ba-150">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678ba-151">-ResourceGroupName</span></span>
<span data-ttu-id="678ba-152">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="678ba-152">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-153">-RunList</span><span class="sxs-lookup"><span data-stu-id="678ba-153">-RunList</span></span>
<span data-ttu-id="678ba-154">指定 [主廚] 節點的 [執行] 清單。</span><span class="sxs-lookup"><span data-stu-id="678ba-154">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-155">密碼</span><span class="sxs-lookup"><span data-stu-id="678ba-155">-Secret</span></span>
<span data-ttu-id="678ba-156">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="678ba-156">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-157">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="678ba-157">-SecretFile</span></span>
<span data-ttu-id="678ba-158">檔案的路徑，該檔案包含用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="678ba-158">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="678ba-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="678ba-160">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="678ba-160">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-161">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="678ba-161">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-162">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="678ba-162">-ValidationPem</span></span>
<span data-ttu-id="678ba-163">指定主廚驗證程式. pem 檔路徑</span><span class="sxs-lookup"><span data-stu-id="678ba-163">Specifies the Chef validator .pem file path</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-164">-VMName</span><span class="sxs-lookup"><span data-stu-id="678ba-164">-VMName</span></span>
<span data-ttu-id="678ba-165">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="678ba-165">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="678ba-166">這個 Cmdlet 會為此參數指定的虛擬機器新增主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="678ba-166">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-167">-Windows</span><span class="sxs-lookup"><span data-stu-id="678ba-167">-Windows</span></span>
<span data-ttu-id="678ba-168">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="678ba-168">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-169">-確認</span><span class="sxs-lookup"><span data-stu-id="678ba-169">-Confirm</span></span>
<span data-ttu-id="678ba-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="678ba-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678ba-171">-WhatIf</span></span>
<span data-ttu-id="678ba-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="678ba-172">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="678ba-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="678ba-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678ba-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678ba-174">CommonParameters</span></span>
<span data-ttu-id="678ba-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="678ba-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678ba-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="678ba-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678ba-177">輸入</span><span class="sxs-lookup"><span data-stu-id="678ba-177">INPUTS</span></span>

### <span data-ttu-id="678ba-178">所有</span><span class="sxs-lookup"><span data-stu-id="678ba-178">None</span></span>
<span data-ttu-id="678ba-179">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="678ba-179">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="678ba-180">輸出</span><span class="sxs-lookup"><span data-stu-id="678ba-180">OUTPUTS</span></span>

## <span data-ttu-id="678ba-181">筆記</span><span class="sxs-lookup"><span data-stu-id="678ba-181">NOTES</span></span>

## <span data-ttu-id="678ba-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="678ba-182">RELATED LINKS</span></span>

[<span data-ttu-id="678ba-183">AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="678ba-183">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="678ba-184">移除-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="678ba-184">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
