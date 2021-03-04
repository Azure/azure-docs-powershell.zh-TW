---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2e0aeb7535f07e9841c9c0a35a131ce0ca7b1a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906942"
---
# <span data-ttu-id="39af2-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="39af2-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="39af2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39af2-102">SYNOPSIS</span></span>
<span data-ttu-id="39af2-103">將擴充功能新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39af2-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="39af2-104">語法</span><span class="sxs-lookup"><span data-stu-id="39af2-104">SYNTAX</span></span>

### <span data-ttu-id="39af2-105">Linux</span><span class="sxs-lookup"><span data-stu-id="39af2-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39af2-106">窗戶</span><span class="sxs-lookup"><span data-stu-id="39af2-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39af2-107">描述</span><span class="sxs-lookup"><span data-stu-id="39af2-107">DESCRIPTION</span></span>
<span data-ttu-id="39af2-108">**Set-Az VIRTUALChefExtension** Cmdlet 會將擴充功能新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39af2-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="39af2-109">例子</span><span class="sxs-lookup"><span data-stu-id="39af2-109">EXAMPLES</span></span>

### <span data-ttu-id="39af2-110">範例 1：新增擴充功能至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="39af2-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="39af2-111">此命令會將一個擴充功能新增到 Windows VIRTUAL Machine，名為 Windows%。。</span><span class="sxs-lookup"><span data-stu-id="39af2-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="39af2-112">當虛擬機器啟動時，系統管理程式會引導虛擬機器執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="39af2-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="39af2-113">範例 2：在 Linux 虛擬機器中新增一個擴充功能</span><span class="sxs-lookup"><span data-stu-id="39af2-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="39af2-114">此命令會將擴充功能新增到 Linux LINUX LINUX001 的 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39af2-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="39af2-115">當虛擬機器啟動時，系統管理程式會引導虛擬機器執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="39af2-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="39af2-116">範例 3：在 Windows 虛擬機器中新增具有 bootstrap 選項的擴充功能</span><span class="sxs-lookup"><span data-stu-id="39af2-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="39af2-117">此命令會將擴充功能新增到 Windows VIRTUAL Machine，名為 Windows%。。</span><span class="sxs-lookup"><span data-stu-id="39af2-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="39af2-118">當虛擬機器啟動時，系統管理程式會引導虛擬機器執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="39af2-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="39af2-119">引導之後，虛擬機器會參照以 JSON 格式指定的 BootstrapOptions。</span><span class="sxs-lookup"><span data-stu-id="39af2-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="39af2-120">參數</span><span class="sxs-lookup"><span data-stu-id="39af2-120">PARAMETERS</span></span>

### <span data-ttu-id="39af2-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="39af2-121">-AutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="39af2-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="39af2-122">-BootstrapOptions</span></span>
<span data-ttu-id="39af2-123">在選項中指定client_rb設定。</span><span class="sxs-lookup"><span data-stu-id="39af2-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="39af2-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="39af2-124">-BootstrapVersion</span></span>
<span data-ttu-id="39af2-125">指定開機配置的版本。</span><span class="sxs-lookup"><span data-stu-id="39af2-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="39af2-126">-有一天，有一天</span><span class="sxs-lookup"><span data-stu-id="39af2-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="39af2-127">指定執行 (服務) 的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="39af2-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="39af2-128">如果您不想在 Azure VM 上安裝系統管理服務，請在此欄位中將值設為 0。</span><span class="sxs-lookup"><span data-stu-id="39af2-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="39af2-129">-因此，一應十四萬美元</span><span class="sxs-lookup"><span data-stu-id="39af2-129">-ChefServerUrl</span></span>
<span data-ttu-id="39af2-130">指定一個 Url 的因此名伺服器連結。</span><span class="sxs-lookup"><span data-stu-id="39af2-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="39af2-131">-Client進位</span><span class="sxs-lookup"><span data-stu-id="39af2-131">-ClientRb</span></span>
<span data-ttu-id="39af2-132">指定一個完整路徑的一個資料，即是一個資料行。</span><span class="sxs-lookup"><span data-stu-id="39af2-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="39af2-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="39af2-133">-Daemon</span></span>
<span data-ttu-id="39af2-134">為自動執行設定管理用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="39af2-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="39af2-135">節點平臺應該是 Windows。</span><span class="sxs-lookup"><span data-stu-id="39af2-135">The node platform should be Windows.</span></span>
<span data-ttu-id="39af2-136">允許的選項：'none'，'service' 和 'task'。</span><span class="sxs-lookup"><span data-stu-id="39af2-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="39af2-137">none - 目前可防止系統將管理用戶端服務當做服務。</span><span class="sxs-lookup"><span data-stu-id="39af2-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="39af2-138">服務 - 將管理用戶端設定為在背景中以服務方式自動執行。</span><span class="sxs-lookup"><span data-stu-id="39af2-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="39af2-139">工作 - 將管理用戶端設定為在背景中自動執行排程任務。</span><span class="sxs-lookup"><span data-stu-id="39af2-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

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

### <span data-ttu-id="39af2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39af2-140">-DefaultProfile</span></span>
<span data-ttu-id="39af2-141">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39af2-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39af2-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="39af2-142">-JsonAttribute</span></span>
<span data-ttu-id="39af2-143">要新增到第一次執行管理用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="39af2-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="39af2-144">例如-JsonAttribute '{"foo" ： "bar"}'</span><span class="sxs-lookup"><span data-stu-id="39af2-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="39af2-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="39af2-145">-Linux</span></span>
<span data-ttu-id="39af2-146">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39af2-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="39af2-147">-位置</span><span class="sxs-lookup"><span data-stu-id="39af2-147">-Location</span></span>
<span data-ttu-id="39af2-148">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="39af2-148">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="39af2-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="39af2-149">-Name</span></span>
<span data-ttu-id="39af2-150">指定擴充功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="39af2-150">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="39af2-151">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39af2-151">-NoWait</span></span>
<span data-ttu-id="39af2-152">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="39af2-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="39af2-153">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="39af2-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="39af2-154">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="39af2-154">-OrganizationName</span></span>
<span data-ttu-id="39af2-155">指定擴充名的組名。</span><span class="sxs-lookup"><span data-stu-id="39af2-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="39af2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39af2-156">-ResourceGroupName</span></span>
<span data-ttu-id="39af2-157">指定包含虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="39af2-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="39af2-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="39af2-158">-RunList</span></span>
<span data-ttu-id="39af2-159">指定主節點執行清單。</span><span class="sxs-lookup"><span data-stu-id="39af2-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="39af2-160">-機密</span><span class="sxs-lookup"><span data-stu-id="39af2-160">-Secret</span></span>
<span data-ttu-id="39af2-161">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="39af2-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="39af2-162">-機密檔</span><span class="sxs-lookup"><span data-stu-id="39af2-162">-SecretFile</span></span>
<span data-ttu-id="39af2-163">包含用來加密及解密資料袋專案值之加密金鑰的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="39af2-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="39af2-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="39af2-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="39af2-165">指定要用於此虛擬機器的擴充功能版本。</span><span class="sxs-lookup"><span data-stu-id="39af2-165">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="39af2-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="39af2-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="39af2-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="39af2-167">-ValidationPem</span></span>
<span data-ttu-id="39af2-168">指定主程式驗證程式 .pem 檔案路徑</span><span class="sxs-lookup"><span data-stu-id="39af2-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="39af2-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="39af2-169">-VMName</span></span>
<span data-ttu-id="39af2-170">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="39af2-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="39af2-171">此 Cmdlet 會新增此參數指定之虛擬機器的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="39af2-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="39af2-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="39af2-172">-Windows</span></span>
<span data-ttu-id="39af2-173">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="39af2-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="39af2-174">-確認</span><span class="sxs-lookup"><span data-stu-id="39af2-174">-Confirm</span></span>
<span data-ttu-id="39af2-175">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39af2-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39af2-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39af2-176">-WhatIf</span></span>
<span data-ttu-id="39af2-177">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39af2-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39af2-178">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39af2-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39af2-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39af2-179">CommonParameters</span></span>
<span data-ttu-id="39af2-180">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39af2-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39af2-181">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39af2-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39af2-182">輸入</span><span class="sxs-lookup"><span data-stu-id="39af2-182">INPUTS</span></span>

### <span data-ttu-id="39af2-183">System.String</span><span class="sxs-lookup"><span data-stu-id="39af2-183">System.String</span></span>

### <span data-ttu-id="39af2-184">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39af2-184">System.Boolean</span></span>

## <span data-ttu-id="39af2-185">輸出</span><span class="sxs-lookup"><span data-stu-id="39af2-185">OUTPUTS</span></span>

### <span data-ttu-id="39af2-186">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="39af2-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="39af2-187">筆記</span><span class="sxs-lookup"><span data-stu-id="39af2-187">NOTES</span></span>

## <span data-ttu-id="39af2-188">相關連結</span><span class="sxs-lookup"><span data-stu-id="39af2-188">RELATED LINKS</span></span>

[<span data-ttu-id="39af2-189">Get-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="39af2-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="39af2-190">Remove-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="39af2-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
