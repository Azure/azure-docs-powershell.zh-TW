---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453955"
---
# <span data-ttu-id="3d3f7-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="3d3f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d3f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3f7-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="3d3f7-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d3f7-104">SYNTAX</span></span>

### <span data-ttu-id="3d3f7-105">S1</span><span class="sxs-lookup"><span data-stu-id="3d3f7-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d3f7-106">S2</span><span class="sxs-lookup"><span data-stu-id="3d3f7-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d3f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="3d3f7-107">DESCRIPTION</span></span>
<span data-ttu-id="3d3f7-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="3d3f7-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="3d3f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d3f7-109">EXAMPLES</span></span>

### <span data-ttu-id="3d3f7-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3d3f7-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="3d3f7-111">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="3d3f7-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3d3f7-112">參數</span><span class="sxs-lookup"><span data-stu-id="3d3f7-112">PARAMETERS</span></span>

### <span data-ttu-id="3d3f7-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3d3f7-113">-AppServicePlan</span></span>
<span data-ttu-id="3d3f7-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="3d3f7-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3d3f7-115">-AppSettings</span></span>
<span data-ttu-id="3d3f7-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="3d3f7-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="3d3f7-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3d3f7-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="3d3f7-118">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3d3f7-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3d3f7-119">-ConnectionStrings</span></span>
<span data-ttu-id="3d3f7-120">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="3d3f7-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3d3f7-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3d3f7-121">-DefaultDocuments</span></span>
<span data-ttu-id="3d3f7-122">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="3d3f7-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="3d3f7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3f7-123">-DefaultProfile</span></span>
<span data-ttu-id="3d3f7-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3d3f7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3f7-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3d3f7-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3d3f7-126">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3d3f7-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3d3f7-127">-HandlerMappings</span></span>
<span data-ttu-id="3d3f7-128">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="3d3f7-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3d3f7-129">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-129">-HostNames</span></span>
<span data-ttu-id="3d3f7-130">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="3d3f7-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="3d3f7-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3d3f7-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3d3f7-132">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3d3f7-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3d3f7-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="3d3f7-134">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3d3f7-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-135">-Name</span></span>
<span data-ttu-id="3d3f7-136">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-136">WebApp Name</span></span>

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

### <span data-ttu-id="3d3f7-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3d3f7-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="3d3f7-138">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="3d3f7-138">Net Framework Version</span></span>

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

### <span data-ttu-id="3d3f7-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3d3f7-139">-NumberOfWorkers</span></span>
<span data-ttu-id="3d3f7-140">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="3d3f7-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3d3f7-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3d3f7-141">-PhpVersion</span></span>
<span data-ttu-id="3d3f7-142">Php 版本</span><span class="sxs-lookup"><span data-stu-id="3d3f7-142">Php Version</span></span>

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

### <span data-ttu-id="3d3f7-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3d3f7-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="3d3f7-144">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="3d3f7-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="3d3f7-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3f7-145">-ResourceGroupName</span></span>
<span data-ttu-id="3d3f7-146">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3d3f7-146">Resource Group Name</span></span>

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

### <span data-ttu-id="3d3f7-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3d3f7-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3d3f7-148">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3d3f7-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-149">-WebApp</span></span>
<span data-ttu-id="3d3f7-150">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="3d3f7-150">WebApp Object</span></span>

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

### <span data-ttu-id="3d3f7-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3d3f7-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="3d3f7-152">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="3d3f7-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d3f7-153">-AsJob</span></span>
<span data-ttu-id="3d3f7-154">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3d3f7-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d3f7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3f7-155">CommonParameters</span></span>
<span data-ttu-id="3d3f7-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d3f7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3f7-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d3f7-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3f7-158">輸入</span><span class="sxs-lookup"><span data-stu-id="3d3f7-158">INPUTS</span></span>

### <span data-ttu-id="3d3f7-159">時會</span><span class="sxs-lookup"><span data-stu-id="3d3f7-159">Int32</span></span>
<span data-ttu-id="3d3f7-160">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="3d3f7-161">網站地圖</span><span class="sxs-lookup"><span data-stu-id="3d3f7-161">Site</span></span>
<span data-ttu-id="3d3f7-162">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="3d3f7-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3d3f7-163">輸出</span><span class="sxs-lookup"><span data-stu-id="3d3f7-163">OUTPUTS</span></span>

## <span data-ttu-id="3d3f7-164">筆記</span><span class="sxs-lookup"><span data-stu-id="3d3f7-164">NOTES</span></span>

## <span data-ttu-id="3d3f7-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d3f7-165">RELATED LINKS</span></span>

[<span data-ttu-id="3d3f7-166">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="3d3f7-167">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="3d3f7-168">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="3d3f7-169">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="3d3f7-170">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="3d3f7-171">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="3d3f7-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
