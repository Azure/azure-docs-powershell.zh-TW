---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: b26ce11a60894ae8bf43b49c1395b4683b0280fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622681"
---
# <span data-ttu-id="b3ce6-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b3ce6-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="b3ce6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ce6-103">新增主廚延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="b3ce6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3ce6-104">SYNTAX</span></span>

### <span data-ttu-id="b3ce6-105">Linux</span><span class="sxs-lookup"><span data-stu-id="b3ce6-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3ce6-106">時間</span><span class="sxs-lookup"><span data-stu-id="b3ce6-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ce6-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="b3ce6-108">**AzVMChefExtension** Cmdlet 會將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="b3ce6-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3ce6-109">EXAMPLES</span></span>

### <span data-ttu-id="b3ce6-110">範例1：新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b3ce6-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="b3ce6-111">這個命令會將主廚延伸新增到名為 WindowsVM001 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="b3ce6-112">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="b3ce6-113">範例2：新增主廚延伸至 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b3ce6-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="b3ce6-114">這個命令會將主廚延伸新增到名為 LinuxVM001 的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="b3ce6-115">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="b3ce6-116">範例3：使用 [引導選項] 新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b3ce6-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="b3ce6-117">這個命令會將主廚延伸新增到名為 WindowsVM002 的 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="b3ce6-118">啟動虛擬機器時，請主廚 bootstraps 虛擬機器來執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="b3ce6-119">在引導之後，虛擬機器會參照 JSON 格式所指定的 BootstrapOptions。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="b3ce6-120">參數</span><span class="sxs-lookup"><span data-stu-id="b3ce6-120">PARAMETERS</span></span>

### <span data-ttu-id="b3ce6-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b3ce6-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="b3ce6-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="b3ce6-122">-BootstrapOptions</span></span>
<span data-ttu-id="b3ce6-123">指定 [client_rb] 選項中的 [設定]。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="b3ce6-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="b3ce6-124">-BootstrapVersion</span></span>
<span data-ttu-id="b3ce6-125">指定啟動配置的版本。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="b3ce6-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="b3ce6-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="b3ce6-127">指定主廚服務執行的頻率 (（分鐘）) 。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="b3ce6-128">如果您不想要在 Azure VM 上安裝主廚服務，請將此欄位中的值設為0。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="b3ce6-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="b3ce6-129">-ChefServerUrl</span></span>
<span data-ttu-id="b3ce6-130">將主廚伺服器連結指定為 URL。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="b3ce6-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="b3ce6-131">-ClientRb</span></span>
<span data-ttu-id="b3ce6-132">指定主廚用戶端. rb 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="b3ce6-133">-守護程式</span><span class="sxs-lookup"><span data-stu-id="b3ce6-133">-Daemon</span></span>
<span data-ttu-id="b3ce6-134">為無人參與的執行設定主廚用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="b3ce6-135">節點平臺應該是 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-135">The node platform should be Windows.</span></span>
<span data-ttu-id="b3ce6-136">允許的選項： "none"、"service" 和 "task"。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="b3ce6-137">none-目前禁止主廚-用戶端服務被設定為服務。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="b3ce6-138">服務-將主廚用戶端設定為在背景中自動執行，成為服務。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="b3ce6-139">任務-將主廚-用戶端自動在背景中做為 secheduled 任務自動執行。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="b3ce6-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ce6-140">-DefaultProfile</span></span>
<span data-ttu-id="b3ce6-141">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ce6-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="b3ce6-142">-JsonAttribute</span></span>
<span data-ttu-id="b3ce6-143">要新增至第一次執行主廚-用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="b3ce6-144">例如，-JsonAttribute "{" foo "：" bar "}"</span><span class="sxs-lookup"><span data-stu-id="b3ce6-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="b3ce6-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="b3ce6-145">-Linux</span></span>
<span data-ttu-id="b3ce6-146">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="b3ce6-147">-位置</span><span class="sxs-lookup"><span data-stu-id="b3ce6-147">-Location</span></span>
<span data-ttu-id="b3ce6-148">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="b3ce6-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3ce6-149">-Name</span></span>
<span data-ttu-id="b3ce6-150">指定主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="b3ce6-151">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="b3ce6-151">-OrganizationName</span></span>
<span data-ttu-id="b3ce6-152">指定主廚延伸的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-152">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="b3ce6-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ce6-153">-ResourceGroupName</span></span>
<span data-ttu-id="b3ce6-154">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="b3ce6-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="b3ce6-155">-RunList</span></span>
<span data-ttu-id="b3ce6-156">指定 [主廚] 節點的 [執行] 清單。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-156">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="b3ce6-157">密碼</span><span class="sxs-lookup"><span data-stu-id="b3ce6-157">-Secret</span></span>
<span data-ttu-id="b3ce6-158">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="b3ce6-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="b3ce6-159">-SecretFile</span></span>
<span data-ttu-id="b3ce6-160">檔案的路徑，該檔案包含用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="b3ce6-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b3ce6-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="b3ce6-162">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-162">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="b3ce6-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="b3ce6-163">-ValidationClientName</span></span>
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

### <span data-ttu-id="b3ce6-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="b3ce6-164">-ValidationPem</span></span>
<span data-ttu-id="b3ce6-165">指定主廚驗證程式. pem 檔路徑</span><span class="sxs-lookup"><span data-stu-id="b3ce6-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="b3ce6-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3ce6-166">-VMName</span></span>
<span data-ttu-id="b3ce6-167">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b3ce6-168">這個 Cmdlet 會為此參數指定的虛擬機器新增主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b3ce6-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="b3ce6-169">-Windows</span></span>
<span data-ttu-id="b3ce6-170">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="b3ce6-171">-確認</span><span class="sxs-lookup"><span data-stu-id="b3ce6-171">-Confirm</span></span>
<span data-ttu-id="b3ce6-172">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3ce6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3ce6-173">-WhatIf</span></span>
<span data-ttu-id="b3ce6-174">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3ce6-175">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3ce6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ce6-176">CommonParameters</span></span>
<span data-ttu-id="b3ce6-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ce6-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3ce6-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ce6-179">輸入</span><span class="sxs-lookup"><span data-stu-id="b3ce6-179">INPUTS</span></span>

### <span data-ttu-id="b3ce6-180">System.object</span><span class="sxs-lookup"><span data-stu-id="b3ce6-180">System.String</span></span>

### <span data-ttu-id="b3ce6-181">System.object</span><span class="sxs-lookup"><span data-stu-id="b3ce6-181">System.Boolean</span></span>

## <span data-ttu-id="b3ce6-182">輸出</span><span class="sxs-lookup"><span data-stu-id="b3ce6-182">OUTPUTS</span></span>

### <span data-ttu-id="b3ce6-183">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b3ce6-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b3ce6-184">筆記</span><span class="sxs-lookup"><span data-stu-id="b3ce6-184">NOTES</span></span>

## <span data-ttu-id="b3ce6-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3ce6-185">RELATED LINKS</span></span>

[<span data-ttu-id="b3ce6-186">AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b3ce6-186">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="b3ce6-187">移除-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="b3ce6-187">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
