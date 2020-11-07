---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801834"
---
# <span data-ttu-id="86370-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="86370-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86370-102">SYNOPSIS</span></span>
<span data-ttu-id="86370-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="86370-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86370-104">句法</span><span class="sxs-lookup"><span data-stu-id="86370-104">SYNTAX</span></span>

### <span data-ttu-id="86370-105">S1</span><span class="sxs-lookup"><span data-stu-id="86370-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86370-106">S2</span><span class="sxs-lookup"><span data-stu-id="86370-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86370-107">說明</span><span class="sxs-lookup"><span data-stu-id="86370-107">DESCRIPTION</span></span>
<span data-ttu-id="86370-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="86370-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="86370-109">示例</span><span class="sxs-lookup"><span data-stu-id="86370-109">EXAMPLES</span></span>

### <span data-ttu-id="86370-110">範例1</span><span class="sxs-lookup"><span data-stu-id="86370-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="86370-111">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="86370-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="86370-112">參數</span><span class="sxs-lookup"><span data-stu-id="86370-112">PARAMETERS</span></span>

### <span data-ttu-id="86370-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="86370-113">-AppServicePlan</span></span>
<span data-ttu-id="86370-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="86370-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="86370-115">-AppSettings</span></span>
<span data-ttu-id="86370-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="86370-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="86370-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="86370-118">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="86370-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="86370-119">-ConnectionStrings</span></span>
<span data-ttu-id="86370-120">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="86370-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="86370-121">-DefaultDocuments</span></span>
<span data-ttu-id="86370-122">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="86370-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86370-123">-DefaultProfile</span></span>
<span data-ttu-id="86370-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="86370-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86370-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="86370-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="86370-126">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="86370-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="86370-127">-HandlerMappings</span></span>
<span data-ttu-id="86370-128">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="86370-128">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="86370-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="86370-130">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="86370-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="86370-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="86370-132">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="86370-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="86370-133">-Name</span></span>
<span data-ttu-id="86370-134">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="86370-134">WebApp Name</span></span>

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

### <span data-ttu-id="86370-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="86370-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="86370-136">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="86370-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="86370-137">-NumberOfWorkers</span></span>
<span data-ttu-id="86370-138">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="86370-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="86370-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="86370-139">-PhpVersion</span></span>
<span data-ttu-id="86370-140">Php 版本</span><span class="sxs-lookup"><span data-stu-id="86370-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="86370-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="86370-142">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="86370-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86370-143">-ResourceGroupName</span></span>
<span data-ttu-id="86370-144">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="86370-144">Resource Group Name</span></span>

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

### <span data-ttu-id="86370-145">-槽</span><span class="sxs-lookup"><span data-stu-id="86370-145">-Slot</span></span>
<span data-ttu-id="86370-146">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="86370-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="86370-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="86370-148">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="86370-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86370-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86370-149">-WebApp</span></span>
<span data-ttu-id="86370-150">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="86370-150">WebApp Object</span></span>

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

### <span data-ttu-id="86370-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="86370-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="86370-152">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="86370-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="86370-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="86370-153">-HttpsOnly</span></span>
<span data-ttu-id="86370-154">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="86370-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="86370-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="86370-155">-AssignIdentity</span></span>
<span data-ttu-id="86370-156">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="86370-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="86370-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86370-157">-AsJob</span></span>
<span data-ttu-id="86370-158">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="86370-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86370-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86370-159">CommonParameters</span></span>
<span data-ttu-id="86370-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86370-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86370-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86370-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86370-162">輸入</span><span class="sxs-lookup"><span data-stu-id="86370-162">INPUTS</span></span>

### <span data-ttu-id="86370-163">時會</span><span class="sxs-lookup"><span data-stu-id="86370-163">Int32</span></span>
<span data-ttu-id="86370-164">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="86370-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="86370-165">網站地圖</span><span class="sxs-lookup"><span data-stu-id="86370-165">Site</span></span>
<span data-ttu-id="86370-166">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="86370-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="86370-167">輸出</span><span class="sxs-lookup"><span data-stu-id="86370-167">OUTPUTS</span></span>

## <span data-ttu-id="86370-168">筆記</span><span class="sxs-lookup"><span data-stu-id="86370-168">NOTES</span></span>

## <span data-ttu-id="86370-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="86370-169">RELATED LINKS</span></span>

[<span data-ttu-id="86370-170">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-171">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-172">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-173">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-174">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-175">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86370-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="86370-176">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="86370-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
