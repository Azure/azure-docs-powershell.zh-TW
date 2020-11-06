---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447108"
---
# <span data-ttu-id="05ff7-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="05ff7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="05ff7-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="05ff7-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ff7-104">句法</span><span class="sxs-lookup"><span data-stu-id="05ff7-104">SYNTAX</span></span>

### <span data-ttu-id="05ff7-105">S1</span><span class="sxs-lookup"><span data-stu-id="05ff7-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05ff7-106">S2</span><span class="sxs-lookup"><span data-stu-id="05ff7-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05ff7-107">說明</span><span class="sxs-lookup"><span data-stu-id="05ff7-107">DESCRIPTION</span></span>
<span data-ttu-id="05ff7-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="05ff7-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="05ff7-109">示例</span><span class="sxs-lookup"><span data-stu-id="05ff7-109">EXAMPLES</span></span>

### <span data-ttu-id="05ff7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="05ff7-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="05ff7-111">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="05ff7-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="05ff7-112">參數</span><span class="sxs-lookup"><span data-stu-id="05ff7-112">PARAMETERS</span></span>

### <span data-ttu-id="05ff7-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05ff7-113">-AppServicePlan</span></span>
<span data-ttu-id="05ff7-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="05ff7-115">-AppSettings</span></span>
<span data-ttu-id="05ff7-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="05ff7-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="05ff7-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="05ff7-118">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="05ff7-119">-ConnectionStrings</span></span>
<span data-ttu-id="05ff7-120">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="05ff7-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="05ff7-121">-DefaultDocuments</span></span>
<span data-ttu-id="05ff7-122">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="05ff7-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05ff7-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="05ff7-124">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="05ff7-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="05ff7-125">-HandlerMappings</span></span>
<span data-ttu-id="05ff7-126">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="05ff7-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="05ff7-127">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-127">-HostNames</span></span>
<span data-ttu-id="05ff7-128">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="05ff7-128">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="05ff7-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="05ff7-130">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="05ff7-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="05ff7-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="05ff7-132">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-133">-Name</span></span>
<span data-ttu-id="05ff7-134">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-134">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="05ff7-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="05ff7-136">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="05ff7-136">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="05ff7-137">-NumberOfWorkers</span></span>
<span data-ttu-id="05ff7-138">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="05ff7-138">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="05ff7-139">-PhpVersion</span></span>
<span data-ttu-id="05ff7-140">Php 版本</span><span class="sxs-lookup"><span data-stu-id="05ff7-140">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="05ff7-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="05ff7-142">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="05ff7-142">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ff7-143">-ResourceGroupName</span></span>
<span data-ttu-id="05ff7-144">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="05ff7-144">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="05ff7-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="05ff7-146">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="05ff7-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-147">-WebApp</span></span>
<span data-ttu-id="05ff7-148">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="05ff7-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="05ff7-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="05ff7-150">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="05ff7-150">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ff7-151">-DefaultProfile</span></span>
<span data-ttu-id="05ff7-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05ff7-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ff7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ff7-153">CommonParameters</span></span>
<span data-ttu-id="05ff7-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05ff7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ff7-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05ff7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ff7-156">輸入</span><span class="sxs-lookup"><span data-stu-id="05ff7-156">INPUTS</span></span>

### <span data-ttu-id="05ff7-157">時會</span><span class="sxs-lookup"><span data-stu-id="05ff7-157">Int32</span></span>
<span data-ttu-id="05ff7-158">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="05ff7-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="05ff7-159">網站地圖</span><span class="sxs-lookup"><span data-stu-id="05ff7-159">Site</span></span>
<span data-ttu-id="05ff7-160">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="05ff7-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="05ff7-161">輸出</span><span class="sxs-lookup"><span data-stu-id="05ff7-161">OUTPUTS</span></span>

## <span data-ttu-id="05ff7-162">筆記</span><span class="sxs-lookup"><span data-stu-id="05ff7-162">NOTES</span></span>

## <span data-ttu-id="05ff7-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="05ff7-163">RELATED LINKS</span></span>

[<span data-ttu-id="05ff7-164">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="05ff7-165">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="05ff7-166">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="05ff7-167">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="05ff7-168">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="05ff7-169">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="05ff7-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
