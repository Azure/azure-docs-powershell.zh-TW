---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966879"
---
# <span data-ttu-id="fb066-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fb066-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="fb066-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb066-102">SYNOPSIS</span></span>
<span data-ttu-id="fb066-103">設定在 Azure 中執行的網站。</span><span class="sxs-lookup"><span data-stu-id="fb066-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="fb066-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb066-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fb066-105">說明</span><span class="sxs-lookup"><span data-stu-id="fb066-105">DESCRIPTION</span></span>
<span data-ttu-id="fb066-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb066-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fb066-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="fb066-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fb066-108">AzureWebsite Cmdlet 會 **設定** 在 Azure 中執行的網站。</span><span class="sxs-lookup"><span data-stu-id="fb066-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="fb066-109">示例</span><span class="sxs-lookup"><span data-stu-id="fb066-109">EXAMPLES</span></span>

### <span data-ttu-id="fb066-110">範例1：啟用網站的 HTTP 記錄</span><span class="sxs-lookup"><span data-stu-id="fb066-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="fb066-111">這個範例會啟用 HTTP 記錄。</span><span class="sxs-lookup"><span data-stu-id="fb066-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="fb066-112">範例2：設定網站的儲存空間認證</span><span class="sxs-lookup"><span data-stu-id="fb066-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="fb066-113">這個範例會在名為 myWebsite 的網站中，使用 AZURE_STORAGE_ACCOUNT 和 AZURE_STORAGE_ACCESS_KEY 的環境變數來設定儲存認證。</span><span class="sxs-lookup"><span data-stu-id="fb066-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="fb066-114">參數</span><span class="sxs-lookup"><span data-stu-id="fb066-114">PARAMETERS</span></span>

### <span data-ttu-id="fb066-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="fb066-115">-AppSettings</span></span>
<span data-ttu-id="fb066-116">指定網站將使用的環境變數。</span><span class="sxs-lookup"><span data-stu-id="fb066-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="fb066-117">-AutoSwapSlotName</span></span>
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

### <span data-ttu-id="fb066-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="fb066-118">-ConnectionStrings</span></span>
<span data-ttu-id="fb066-119">指定網站所使用的連線字串。</span><span class="sxs-lookup"><span data-stu-id="fb066-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="fb066-120">-DefaultDocuments</span></span>
<span data-ttu-id="fb066-121">指定流覽網站時自動顯示的檔。</span><span class="sxs-lookup"><span data-stu-id="fb066-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fb066-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="fb066-123">決定是否針對網站記錄詳細的 IIS 錯誤。</span><span class="sxs-lookup"><span data-stu-id="fb066-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="fb066-124">-HandlerMappings</span></span>
<span data-ttu-id="fb066-125">指定網站所使用的處理常式映射。</span><span class="sxs-lookup"><span data-stu-id="fb066-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-126">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="fb066-126">-HostNames</span></span>
<span data-ttu-id="fb066-127">指定可用於存取網站的完整主機名稱。</span><span class="sxs-lookup"><span data-stu-id="fb066-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="fb066-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="fb066-129">判斷是否已針對網站啟用 HTTP 記錄。</span><span class="sxs-lookup"><span data-stu-id="fb066-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="fb066-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="fb066-131">指定受管理的管線模式。</span><span class="sxs-lookup"><span data-stu-id="fb066-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-132">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="fb066-132">-Metadata</span></span>
<span data-ttu-id="fb066-133">指定網站的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fb066-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb066-134">-Name</span></span>
<span data-ttu-id="fb066-135">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb066-135">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="fb066-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="fb066-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="fb066-137">指定網站所需的 .Net Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="fb066-137">Specifies the version of the .Net Framework required by the website.</span></span>

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

### <span data-ttu-id="fb066-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="fb066-138">-NumberOfWorkers</span></span>
<span data-ttu-id="fb066-139">指定執行網站的工作進程數。</span><span class="sxs-lookup"><span data-stu-id="fb066-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb066-140">-PassThru</span></span>
<span data-ttu-id="fb066-141">表示此 Cmdlet 會傳回 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="fb066-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="fb066-142">-PhpVersion</span></span>
<span data-ttu-id="fb066-143">指定網站所需的 PHP 版本。</span><span class="sxs-lookup"><span data-stu-id="fb066-143">Specifies the PHP version required by the website.</span></span>

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

### <span data-ttu-id="fb066-144">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fb066-144">-Profile</span></span>
<span data-ttu-id="fb066-145">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fb066-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb066-146">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fb066-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb066-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="fb066-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="fb066-148">判斷是否已啟用網站的要求追蹤功能。</span><span class="sxs-lookup"><span data-stu-id="fb066-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="fb066-149">-RoutingRules</span></span>
<span data-ttu-id="fb066-150">指定要用於在生產中測試的路由規則。</span><span class="sxs-lookup"><span data-stu-id="fb066-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="fb066-151">-SiteWithConfig</span></span>
<span data-ttu-id="fb066-152">指定網站使用的配置。</span><span class="sxs-lookup"><span data-stu-id="fb066-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-153">-槽</span><span class="sxs-lookup"><span data-stu-id="fb066-153">-Slot</span></span>
<span data-ttu-id="fb066-154">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="fb066-154">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="fb066-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="fb066-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="fb066-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="fb066-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="fb066-158">指定是否要啟用32位模式。</span><span class="sxs-lookup"><span data-stu-id="fb066-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="fb066-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="fb066-160">指定是否要啟用 Websocket。</span><span class="sxs-lookup"><span data-stu-id="fb066-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb066-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb066-161">CommonParameters</span></span>
<span data-ttu-id="fb066-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb066-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb066-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb066-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb066-164">輸入</span><span class="sxs-lookup"><span data-stu-id="fb066-164">INPUTS</span></span>

## <span data-ttu-id="fb066-165">輸出</span><span class="sxs-lookup"><span data-stu-id="fb066-165">OUTPUTS</span></span>

## <span data-ttu-id="fb066-166">筆記</span><span class="sxs-lookup"><span data-stu-id="fb066-166">NOTES</span></span>

## <span data-ttu-id="fb066-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb066-167">RELATED LINKS</span></span>

[<span data-ttu-id="fb066-168">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fb066-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="fb066-169">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fb066-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="fb066-170">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fb066-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


