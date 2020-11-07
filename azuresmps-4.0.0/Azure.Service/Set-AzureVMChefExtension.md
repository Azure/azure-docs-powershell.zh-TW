---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967491"
---
# <span data-ttu-id="0d512-101">Set-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0d512-101">Set-AzureVMChefExtension</span></span>

## <span data-ttu-id="0d512-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d512-102">SYNOPSIS</span></span>
<span data-ttu-id="0d512-103">將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-103">Adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="0d512-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d512-104">SYNTAX</span></span>

### <span data-ttu-id="0d512-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="0d512-105">Windows (Default)</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d512-106">Linux</span><span class="sxs-lookup"><span data-stu-id="0d512-106">Linux</span></span>
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d512-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d512-107">DESCRIPTION</span></span>
<span data-ttu-id="0d512-108">**AzureVMChefExtension** Cmdlet 會將主廚延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="0d512-109">示例</span><span class="sxs-lookup"><span data-stu-id="0d512-109">EXAMPLES</span></span>

### <span data-ttu-id="0d512-110">範例1：新增主廚延伸至 Windows 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="0d512-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

<span data-ttu-id="0d512-111">這個命令會將主廚延伸新增至 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-111">This command adds a Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="0d512-112">當虛擬機器出現時，它會引導您使用主廚，並在其上執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="0d512-112">When the virtual machine comes up, it is bootstrapped with Chef and runs Apache on it.</span></span>

### <span data-ttu-id="0d512-113">範例2：使用引導在 Windows 虛擬機器中新增主廚延伸功能</span><span class="sxs-lookup"><span data-stu-id="0d512-113">Example 2: Add a Chef extension to a Windows virtual machine with bootstrapping</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

<span data-ttu-id="0d512-114">這個命令會將主廚延伸新增至 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-114">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="0d512-115">當虛擬機器啟動時，會使用主廚引導，並在其上執行 Apache。</span><span class="sxs-lookup"><span data-stu-id="0d512-115">When the virtual machine launches, it is bootstrapped with Chef and runs Apache on it.</span></span>
<span data-ttu-id="0d512-116">在引導之後，虛擬機器會參照 JSON 格式所指定的 *BootstrapOptions* 。</span><span class="sxs-lookup"><span data-stu-id="0d512-116">After bootstrapping, the virtual machine refers to the *BootstrapOptions* specified in JSON format.</span></span>

### <span data-ttu-id="0d512-117">範例3：新增主廚延伸至 Windows 虛擬機器並安裝 Apache 與 GIT</span><span class="sxs-lookup"><span data-stu-id="0d512-117">Example 3: Add a Chef extension to a Windows virtual machine and install Apache and GIT</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

<span data-ttu-id="0d512-118">這個命令會將主廚延伸新增至 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-118">This command adds the Chef extension to a Windows virtual machine.</span></span>
<span data-ttu-id="0d512-119">當虛擬機器啟動時，會使用主廚引導，且已安裝 Apache 和 GIT。</span><span class="sxs-lookup"><span data-stu-id="0d512-119">When the virtual machine launches, it is bootstrapped with Chef and have Apache and GIT installed.</span></span>
<span data-ttu-id="0d512-120">如果您沒有提供用戶端 rb，您必須提供主廚 server URL 和驗證用戶端名稱。</span><span class="sxs-lookup"><span data-stu-id="0d512-120">If you do not provide the client.rb, you need to provide the Chef server URL and validation client name.</span></span>

### <span data-ttu-id="0d512-121">範例4：新增主廚延伸至 Linux 虛擬機器</span><span class="sxs-lookup"><span data-stu-id="0d512-121">Example 4: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

<span data-ttu-id="0d512-122">這個命令會將主廚延伸新增至 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-122">This command adds the Chef extension to a Linux virtual machine.</span></span>
<span data-ttu-id="0d512-123">當虛擬機器啟動時，會使用主廚引導它。</span><span class="sxs-lookup"><span data-stu-id="0d512-123">When the virtual machine launches, it is bootstrapped with Chef.</span></span>
<span data-ttu-id="0d512-124">如果您沒有提供用戶端 rb，您必須提供主廚伺服器 URL 與組織。</span><span class="sxs-lookup"><span data-stu-id="0d512-124">If you do not provide the client.rb, you need to provide the Chef server URL and organization.</span></span>

## <span data-ttu-id="0d512-125">參數</span><span class="sxs-lookup"><span data-stu-id="0d512-125">PARAMETERS</span></span>

### <span data-ttu-id="0d512-126">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="0d512-126">-BootstrapOptions</span></span>
<span data-ttu-id="0d512-127">指定 JavaScript 物件符號 (JSON) 格式中的 [引導] 選項。</span><span class="sxs-lookup"><span data-stu-id="0d512-127">Specifies bootstrap options in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="0d512-128">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="0d512-128">-BootstrapVersion</span></span>
<span data-ttu-id="0d512-129">指定與副檔名一起安裝的主廚用戶端版本。</span><span class="sxs-lookup"><span data-stu-id="0d512-129">Specifies the version of the Chef client that is installed together with the extension.</span></span>

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

### <span data-ttu-id="0d512-130">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="0d512-130">-ChefDaemonInterval</span></span>
<span data-ttu-id="0d512-131">指定主廚服務執行的頻率 (（分鐘）) 。</span><span class="sxs-lookup"><span data-stu-id="0d512-131">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="0d512-132">如果您不想要在 Azure VM 上安裝主廚服務，請將此欄位中的值設為0。</span><span class="sxs-lookup"><span data-stu-id="0d512-132">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

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

### <span data-ttu-id="0d512-133">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="0d512-133">-ChefServerUrl</span></span>
<span data-ttu-id="0d512-134">指定主廚伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="0d512-134">Specifies the URL of the Chef server.</span></span>

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

### <span data-ttu-id="0d512-135">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="0d512-135">-ClientRb</span></span>
<span data-ttu-id="0d512-136">指定主廚用戶端. rb 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0d512-136">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="0d512-137">-守護程式</span><span class="sxs-lookup"><span data-stu-id="0d512-137">-Daemon</span></span>
<span data-ttu-id="0d512-138">為無人參與的執行設定主廚用戶端服務。</span><span class="sxs-lookup"><span data-stu-id="0d512-138">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="0d512-139">節點平臺應該是 [Windows]。</span><span class="sxs-lookup"><span data-stu-id="0d512-139">The node platform should be Windows.</span></span>
<span data-ttu-id="0d512-140">允許的選項： "none"、"service" 和 "task"。</span><span class="sxs-lookup"><span data-stu-id="0d512-140">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="0d512-141">none-目前禁止主廚-用戶端服務被設定為服務。</span><span class="sxs-lookup"><span data-stu-id="0d512-141">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="0d512-142">服務-將主廚用戶端設定為在背景中自動執行，成為服務。</span><span class="sxs-lookup"><span data-stu-id="0d512-142">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="0d512-143">任務-將主廚-用戶端自動在背景中做為 secheduled 任務自動執行。</span><span class="sxs-lookup"><span data-stu-id="0d512-143">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

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

### <span data-ttu-id="0d512-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0d512-144">-InformationAction</span></span>
<span data-ttu-id="0d512-145">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="0d512-145">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0d512-146">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d512-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d512-147">持續</span><span class="sxs-lookup"><span data-stu-id="0d512-147">Continue</span></span>
- <span data-ttu-id="0d512-148">理會</span><span class="sxs-lookup"><span data-stu-id="0d512-148">Ignore</span></span>
- <span data-ttu-id="0d512-149">看</span><span class="sxs-lookup"><span data-stu-id="0d512-149">Inquire</span></span>
- <span data-ttu-id="0d512-150">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d512-150">SilentlyContinue</span></span>
- <span data-ttu-id="0d512-151">停止</span><span class="sxs-lookup"><span data-stu-id="0d512-151">Stop</span></span>
- <span data-ttu-id="0d512-152">封存</span><span class="sxs-lookup"><span data-stu-id="0d512-152">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d512-153">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d512-153">-InformationVariable</span></span>
<span data-ttu-id="0d512-154">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="0d512-154">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d512-155">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="0d512-155">-JsonAttribute</span></span>
<span data-ttu-id="0d512-156">要新增至第一次執行主廚-用戶端的 JSON 字串。</span><span class="sxs-lookup"><span data-stu-id="0d512-156">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="0d512-157">例如，-JsonAttribute "{" foo "：" bar "}"</span><span class="sxs-lookup"><span data-stu-id="0d512-157">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="0d512-158">-Linux</span><span class="sxs-lookup"><span data-stu-id="0d512-158">-Linux</span></span>
<span data-ttu-id="0d512-159">表示此 Cmdlet 會建立以 Linux 為基礎的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-159">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="0d512-160">-OrganizationName</span><span class="sxs-lookup"><span data-stu-id="0d512-160">-OrganizationName</span></span>
<span data-ttu-id="0d512-161">指定主廚延伸的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="0d512-161">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="0d512-162">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0d512-162">-Profile</span></span>
<span data-ttu-id="0d512-163">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d512-163">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0d512-164">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0d512-164">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d512-165">-RunList</span><span class="sxs-lookup"><span data-stu-id="0d512-165">-RunList</span></span>
<span data-ttu-id="0d512-166">指定 [主廚] 節點的 [執行] 清單。</span><span class="sxs-lookup"><span data-stu-id="0d512-166">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="0d512-167">密碼</span><span class="sxs-lookup"><span data-stu-id="0d512-167">-Secret</span></span>
<span data-ttu-id="0d512-168">用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0d512-168">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="0d512-169">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="0d512-169">-SecretFile</span></span>
<span data-ttu-id="0d512-170">檔案的路徑，該檔案包含用來加密和解密資料袋專案值的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="0d512-170">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="0d512-171">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="0d512-171">-ValidationClientName</span></span>
<span data-ttu-id="0d512-172">指定驗證用戶端的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d512-172">Specifies the name of the validation client.</span></span>

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

### <span data-ttu-id="0d512-173">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="0d512-173">-ValidationPem</span></span>
<span data-ttu-id="0d512-174">指定主廚驗證程式. pem 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="0d512-174">Specifies the Chef validator .pem file path.</span></span>

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

### <span data-ttu-id="0d512-175">-版本</span><span class="sxs-lookup"><span data-stu-id="0d512-175">-Version</span></span>
<span data-ttu-id="0d512-176">指定主廚延伸的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0d512-176">Specifies the version number of the Chef extension.</span></span>

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

### <span data-ttu-id="0d512-177">-VM</span><span class="sxs-lookup"><span data-stu-id="0d512-177">-VM</span></span>
<span data-ttu-id="0d512-178">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="0d512-178">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d512-179">-Windows</span><span class="sxs-lookup"><span data-stu-id="0d512-179">-Windows</span></span>
<span data-ttu-id="0d512-180">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0d512-180">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="0d512-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d512-181">CommonParameters</span></span>
<span data-ttu-id="0d512-182">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d512-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d512-183">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d512-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d512-184">輸入</span><span class="sxs-lookup"><span data-stu-id="0d512-184">INPUTS</span></span>

## <span data-ttu-id="0d512-185">輸出</span><span class="sxs-lookup"><span data-stu-id="0d512-185">OUTPUTS</span></span>

## <span data-ttu-id="0d512-186">筆記</span><span class="sxs-lookup"><span data-stu-id="0d512-186">NOTES</span></span>

## <span data-ttu-id="0d512-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d512-187">RELATED LINKS</span></span>

[<span data-ttu-id="0d512-188">AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0d512-188">Get-AzureVMChefExtension</span></span>](./Get-AzureVMChefExtension.md)

[<span data-ttu-id="0d512-189">移除-AzureVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="0d512-189">Remove-AzureVMChefExtension</span></span>](./Remove-AzureVMChefExtension.md)


