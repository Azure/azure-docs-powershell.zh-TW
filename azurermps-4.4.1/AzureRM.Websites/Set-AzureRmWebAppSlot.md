---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623494"
---
# <span data-ttu-id="ad43d-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ad43d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad43d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad43d-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="ad43d-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad43d-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad43d-104">SYNTAX</span></span>

### <span data-ttu-id="ad43d-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad43d-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad43d-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad43d-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad43d-107">說明</span><span class="sxs-lookup"><span data-stu-id="ad43d-107">DESCRIPTION</span></span>
<span data-ttu-id="ad43d-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="ad43d-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="ad43d-109">示例</span><span class="sxs-lookup"><span data-stu-id="ad43d-109">EXAMPLES</span></span>

### <span data-ttu-id="ad43d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ad43d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="ad43d-111">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="ad43d-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ad43d-112">參數</span><span class="sxs-lookup"><span data-stu-id="ad43d-112">PARAMETERS</span></span>

### <span data-ttu-id="ad43d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad43d-113">-AppServicePlan</span></span>
<span data-ttu-id="ad43d-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-114">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="ad43d-115">-AppSettings</span></span>
<span data-ttu-id="ad43d-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="ad43d-116">App Settings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="ad43d-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="ad43d-118">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-118">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="ad43d-119">-ConnectionStrings</span></span>
<span data-ttu-id="ad43d-120">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="ad43d-120">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="ad43d-121">-DefaultDocuments</span></span>
<span data-ttu-id="ad43d-122">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="ad43d-122">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad43d-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="ad43d-124">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="ad43d-124">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="ad43d-125">-HandlerMappings</span></span>
<span data-ttu-id="ad43d-126">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="ad43d-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="ad43d-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad43d-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="ad43d-128">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="ad43d-128">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="ad43d-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="ad43d-130">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-130">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-131">-Name</span></span>
<span data-ttu-id="ad43d-132">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-132">WebApp Name</span></span>

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

### <span data-ttu-id="ad43d-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="ad43d-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="ad43d-134">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="ad43d-134">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="ad43d-135">-NumberOfWorkers</span></span>
<span data-ttu-id="ad43d-136">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="ad43d-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="ad43d-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="ad43d-137">-PhpVersion</span></span>
<span data-ttu-id="ad43d-138">Php 版本</span><span class="sxs-lookup"><span data-stu-id="ad43d-138">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="ad43d-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="ad43d-140">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="ad43d-140">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad43d-141">-ResourceGroupName</span></span>
<span data-ttu-id="ad43d-142">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-142">Resource Group Name</span></span>

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

### <span data-ttu-id="ad43d-143">-槽</span><span class="sxs-lookup"><span data-stu-id="ad43d-143">-Slot</span></span>
<span data-ttu-id="ad43d-144">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="ad43d-144">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="ad43d-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="ad43d-146">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="ad43d-146">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad43d-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad43d-147">-WebApp</span></span>
<span data-ttu-id="ad43d-148">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="ad43d-148">WebApp Object</span></span>

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

### <span data-ttu-id="ad43d-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="ad43d-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="ad43d-150">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="ad43d-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="ad43d-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad43d-151">-DefaultProfile</span></span>
<span data-ttu-id="ad43d-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad43d-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad43d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad43d-153">CommonParameters</span></span>
<span data-ttu-id="ad43d-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad43d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad43d-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad43d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad43d-156">輸入</span><span class="sxs-lookup"><span data-stu-id="ad43d-156">INPUTS</span></span>

### <span data-ttu-id="ad43d-157">時會</span><span class="sxs-lookup"><span data-stu-id="ad43d-157">Int32</span></span>
<span data-ttu-id="ad43d-158">形參 "NumberOfWorkers" 接受管線中 "Int32" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ad43d-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="ad43d-159">網站地圖</span><span class="sxs-lookup"><span data-stu-id="ad43d-159">Site</span></span>
<span data-ttu-id="ad43d-160">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ad43d-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ad43d-161">輸出</span><span class="sxs-lookup"><span data-stu-id="ad43d-161">OUTPUTS</span></span>

## <span data-ttu-id="ad43d-162">筆記</span><span class="sxs-lookup"><span data-stu-id="ad43d-162">NOTES</span></span>

## <span data-ttu-id="ad43d-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad43d-163">RELATED LINKS</span></span>

[<span data-ttu-id="ad43d-164">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-165">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-166">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-167">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-168">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-169">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad43d-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad43d-170">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad43d-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
