---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4478083a2ee98eceda08012b4346f3ece1657963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794942"
---
# <span data-ttu-id="e46b9-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-101">Set-AzWebApp</span></span>

## <span data-ttu-id="e46b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e46b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e46b9-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="e46b9-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="e46b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e46b9-104">SYNTAX</span></span>

### <span data-ttu-id="e46b9-105">S1</span><span class="sxs-lookup"><span data-stu-id="e46b9-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e46b9-106">S2</span><span class="sxs-lookup"><span data-stu-id="e46b9-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e46b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="e46b9-107">DESCRIPTION</span></span>
<span data-ttu-id="e46b9-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="e46b9-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="e46b9-109">示例</span><span class="sxs-lookup"><span data-stu-id="e46b9-109">EXAMPLES</span></span>

### <span data-ttu-id="e46b9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e46b9-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="e46b9-111">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="e46b9-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e46b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="e46b9-112">PARAMETERS</span></span>

### <span data-ttu-id="e46b9-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e46b9-113">-AppServicePlan</span></span>
<span data-ttu-id="e46b9-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e46b9-115">-AppSettings</span></span>
<span data-ttu-id="e46b9-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="e46b9-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e46b9-117">-AsJob</span></span>
<span data-ttu-id="e46b9-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e46b9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e46b9-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e46b9-119">-AssignIdentity</span></span>
<span data-ttu-id="e46b9-120">在現有的 azure webapp 或 functionapp 上啟用/停用 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="e46b9-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e46b9-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="e46b9-122">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e46b9-123">-ConnectionStrings</span></span>
<span data-ttu-id="e46b9-124">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="e46b9-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e46b9-125">-DefaultDocuments</span></span>
<span data-ttu-id="e46b9-126">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="e46b9-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46b9-127">-DefaultProfile</span></span>
<span data-ttu-id="e46b9-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e46b9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e46b9-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e46b9-130">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="e46b9-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e46b9-131">-HandlerMappings</span></span>
<span data-ttu-id="e46b9-132">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="e46b9-132">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-133">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-133">-HostNames</span></span>
<span data-ttu-id="e46b9-134">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="e46b9-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e46b9-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e46b9-136">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="e46b9-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e46b9-137">-HttpsOnly</span></span>
<span data-ttu-id="e46b9-138">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="e46b9-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e46b9-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="e46b9-140">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-141">-Name</span></span>
<span data-ttu-id="e46b9-142">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e46b9-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="e46b9-144">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="e46b9-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e46b9-145">-NumberOfWorkers</span></span>
<span data-ttu-id="e46b9-146">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="e46b9-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e46b9-147">-PhpVersion</span></span>
<span data-ttu-id="e46b9-148">Php 版本</span><span class="sxs-lookup"><span data-stu-id="e46b9-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e46b9-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="e46b9-150">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="e46b9-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46b9-151">-ResourceGroupName</span></span>
<span data-ttu-id="e46b9-152">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e46b9-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e46b9-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e46b9-154">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="e46b9-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-155">-WebApp</span></span>
<span data-ttu-id="e46b9-156">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="e46b9-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e46b9-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="e46b9-158">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="e46b9-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46b9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46b9-159">CommonParameters</span></span>
<span data-ttu-id="e46b9-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e46b9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46b9-161">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e46b9-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46b9-162">輸入</span><span class="sxs-lookup"><span data-stu-id="e46b9-162">INPUTS</span></span>

### <span data-ttu-id="e46b9-163">時會</span><span class="sxs-lookup"><span data-stu-id="e46b9-163">Int32</span></span>
<span data-ttu-id="e46b9-164">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e46b9-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="e46b9-165">網站地圖</span><span class="sxs-lookup"><span data-stu-id="e46b9-165">Site</span></span>
<span data-ttu-id="e46b9-166">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e46b9-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e46b9-167">輸出</span><span class="sxs-lookup"><span data-stu-id="e46b9-167">OUTPUTS</span></span>

## <span data-ttu-id="e46b9-168">筆記</span><span class="sxs-lookup"><span data-stu-id="e46b9-168">NOTES</span></span>

## <span data-ttu-id="e46b9-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="e46b9-169">RELATED LINKS</span></span>

[<span data-ttu-id="e46b9-170">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-170">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e46b9-171">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-171">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e46b9-172">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-172">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e46b9-173">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-173">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e46b9-174">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-174">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e46b9-175">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e46b9-175">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
