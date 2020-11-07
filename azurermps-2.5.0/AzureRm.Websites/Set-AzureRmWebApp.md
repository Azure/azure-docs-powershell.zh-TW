---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800610"
---
# <span data-ttu-id="40c0b-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="40c0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="40c0b-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="40c0b-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="40c0b-104">SYNTAX</span></span>

### <span data-ttu-id="40c0b-105">S1</span><span class="sxs-lookup"><span data-stu-id="40c0b-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40c0b-106">S2</span><span class="sxs-lookup"><span data-stu-id="40c0b-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40c0b-107">說明</span><span class="sxs-lookup"><span data-stu-id="40c0b-107">DESCRIPTION</span></span>
<span data-ttu-id="40c0b-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="40c0b-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="40c0b-109">示例</span><span class="sxs-lookup"><span data-stu-id="40c0b-109">EXAMPLES</span></span>

### <span data-ttu-id="40c0b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="40c0b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="40c0b-111">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="40c0b-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="40c0b-112">參數</span><span class="sxs-lookup"><span data-stu-id="40c0b-112">PARAMETERS</span></span>

### <span data-ttu-id="40c0b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="40c0b-113">-AppServicePlan</span></span>
<span data-ttu-id="40c0b-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="40c0b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="40c0b-115">-AppSettings</span></span>
<span data-ttu-id="40c0b-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="40c0b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="40c0b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c0b-117">-AsJob</span></span>
<span data-ttu-id="40c0b-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40c0b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40c0b-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="40c0b-119">-AssignIdentity</span></span>
<span data-ttu-id="40c0b-120">在現有的 azure webapp 或 functionapp 上啟用/停用 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="40c0b-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

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

### <span data-ttu-id="40c0b-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="40c0b-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="40c0b-122">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="40c0b-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="40c0b-123">-ConnectionStrings</span></span>
<span data-ttu-id="40c0b-124">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="40c0b-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="40c0b-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="40c0b-125">-DefaultDocuments</span></span>
<span data-ttu-id="40c0b-126">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="40c0b-126">Default Documents String Array</span></span>

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

### <span data-ttu-id="40c0b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c0b-127">-DefaultProfile</span></span>
<span data-ttu-id="40c0b-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40c0b-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40c0b-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="40c0b-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="40c0b-130">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="40c0b-130">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="40c0b-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="40c0b-131">-HandlerMappings</span></span>
<span data-ttu-id="40c0b-132">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="40c0b-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="40c0b-133">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-133">-HostNames</span></span>
<span data-ttu-id="40c0b-134">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="40c0b-134">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="40c0b-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="40c0b-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="40c0b-136">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="40c0b-136">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="40c0b-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="40c0b-137">-HttpsOnly</span></span>
<span data-ttu-id="40c0b-138">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="40c0b-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="40c0b-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="40c0b-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="40c0b-140">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-140">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="40c0b-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-141">-Name</span></span>
<span data-ttu-id="40c0b-142">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-142">WebApp Name</span></span>

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

### <span data-ttu-id="40c0b-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="40c0b-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="40c0b-144">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="40c0b-144">Net Framework Version</span></span>

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

### <span data-ttu-id="40c0b-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="40c0b-145">-NumberOfWorkers</span></span>
<span data-ttu-id="40c0b-146">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="40c0b-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="40c0b-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="40c0b-147">-PhpVersion</span></span>
<span data-ttu-id="40c0b-148">Php 版本</span><span class="sxs-lookup"><span data-stu-id="40c0b-148">Php Version</span></span>

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

### <span data-ttu-id="40c0b-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="40c0b-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="40c0b-150">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="40c0b-150">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="40c0b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c0b-151">-ResourceGroupName</span></span>
<span data-ttu-id="40c0b-152">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="40c0b-152">Resource Group Name</span></span>

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

### <span data-ttu-id="40c0b-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="40c0b-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="40c0b-154">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="40c0b-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="40c0b-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-155">-WebApp</span></span>
<span data-ttu-id="40c0b-156">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="40c0b-156">WebApp Object</span></span>

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

### <span data-ttu-id="40c0b-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="40c0b-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="40c0b-158">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="40c0b-158">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="40c0b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c0b-159">CommonParameters</span></span>
<span data-ttu-id="40c0b-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40c0b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c0b-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40c0b-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c0b-162">輸入</span><span class="sxs-lookup"><span data-stu-id="40c0b-162">INPUTS</span></span>

### <span data-ttu-id="40c0b-163">時會</span><span class="sxs-lookup"><span data-stu-id="40c0b-163">Int32</span></span>
<span data-ttu-id="40c0b-164">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="40c0b-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="40c0b-165">網站地圖</span><span class="sxs-lookup"><span data-stu-id="40c0b-165">Site</span></span>
<span data-ttu-id="40c0b-166">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="40c0b-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="40c0b-167">輸出</span><span class="sxs-lookup"><span data-stu-id="40c0b-167">OUTPUTS</span></span>

## <span data-ttu-id="40c0b-168">筆記</span><span class="sxs-lookup"><span data-stu-id="40c0b-168">NOTES</span></span>

## <span data-ttu-id="40c0b-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="40c0b-169">RELATED LINKS</span></span>

[<span data-ttu-id="40c0b-170">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="40c0b-171">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="40c0b-172">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="40c0b-173">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="40c0b-174">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="40c0b-175">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="40c0b-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
