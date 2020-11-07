---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793353"
---
# <span data-ttu-id="b8c11-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="b8c11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c11-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c11-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="b8c11-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="b8c11-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c11-104">SYNTAX</span></span>

### <span data-ttu-id="b8c11-105">S1</span><span class="sxs-lookup"><span data-stu-id="b8c11-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8c11-106">S2</span><span class="sxs-lookup"><span data-stu-id="b8c11-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c11-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8c11-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c11-108">**AzWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="b8c11-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="b8c11-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8c11-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c11-110">範例1</span><span class="sxs-lookup"><span data-stu-id="b8c11-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="b8c11-111">這個命令會變更與 Slot001 相關聯的 appservice 方案（與資源群組預設-Web-WestUS 相關的 Webapp ContosoWebApp）。</span><span class="sxs-lookup"><span data-stu-id="b8c11-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="b8c11-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="b8c11-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="b8c11-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="b8c11-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="b8c11-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b8c11-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="b8c11-115">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="b8c11-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="b8c11-116">參數</span><span class="sxs-lookup"><span data-stu-id="b8c11-116">PARAMETERS</span></span>

### <span data-ttu-id="b8c11-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8c11-117">-AppServicePlan</span></span>
<span data-ttu-id="b8c11-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="b8c11-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="b8c11-119">-AppSettings</span></span>
<span data-ttu-id="b8c11-120">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b8c11-120">App Settings HashTable.</span></span> <span data-ttu-id="b8c11-121">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="b8c11-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="b8c11-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c11-122">-AsJob</span></span>
<span data-ttu-id="b8c11-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b8c11-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8c11-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c11-124">-AssignIdentity</span></span>
<span data-ttu-id="b8c11-125">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="b8c11-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="b8c11-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="b8c11-127">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="b8c11-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="b8c11-128">-AzureStoragePath</span></span>
<span data-ttu-id="b8c11-129">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="b8c11-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="b8c11-130">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="b8c11-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="b8c11-131">-ConnectionStrings</span></span>
<span data-ttu-id="b8c11-132">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="b8c11-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="b8c11-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="b8c11-133">-ContainerImageName</span></span>
<span data-ttu-id="b8c11-134">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-134">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="b8c11-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="b8c11-136">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="b8c11-136">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="b8c11-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="b8c11-138">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="b8c11-138">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="b8c11-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="b8c11-140">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-140">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="b8c11-141">-DefaultDocuments</span></span>
<span data-ttu-id="b8c11-142">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="b8c11-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="b8c11-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c11-143">-DefaultProfile</span></span>
<span data-ttu-id="b8c11-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8c11-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c11-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b8c11-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="b8c11-146">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="b8c11-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="b8c11-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="b8c11-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="b8c11-148">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="b8c11-148">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="b8c11-149">-HandlerMappings</span></span>
<span data-ttu-id="b8c11-150">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="b8c11-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="b8c11-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="b8c11-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="b8c11-152">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="b8c11-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="b8c11-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b8c11-153">-HttpsOnly</span></span>
<span data-ttu-id="b8c11-154">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8c11-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="b8c11-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="b8c11-156">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="b8c11-157">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-157">-Name</span></span>
<span data-ttu-id="b8c11-158">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-158">WebApp Name</span></span>

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

### <span data-ttu-id="b8c11-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="b8c11-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="b8c11-160">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="b8c11-160">Net Framework Version</span></span>

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

### <span data-ttu-id="b8c11-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="b8c11-161">-NumberOfWorkers</span></span>
<span data-ttu-id="b8c11-162">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="b8c11-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="b8c11-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="b8c11-163">-PhpVersion</span></span>
<span data-ttu-id="b8c11-164">Php 版本</span><span class="sxs-lookup"><span data-stu-id="b8c11-164">Php Version</span></span>

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

### <span data-ttu-id="b8c11-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="b8c11-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="b8c11-166">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="b8c11-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="b8c11-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c11-167">-ResourceGroupName</span></span>
<span data-ttu-id="b8c11-168">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-168">Resource Group Name</span></span>

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

### <span data-ttu-id="b8c11-169">-槽</span><span class="sxs-lookup"><span data-stu-id="b8c11-169">-Slot</span></span>
<span data-ttu-id="b8c11-170">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="b8c11-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b8c11-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="b8c11-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="b8c11-172">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="b8c11-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="b8c11-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b8c11-173">-WebApp</span></span>
<span data-ttu-id="b8c11-174">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="b8c11-174">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c11-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="b8c11-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="b8c11-176">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="b8c11-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="b8c11-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c11-177">CommonParameters</span></span>
<span data-ttu-id="b8c11-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c11-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c11-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8c11-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c11-180">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c11-180">INPUTS</span></span>

### <span data-ttu-id="b8c11-181">System.object</span><span class="sxs-lookup"><span data-stu-id="b8c11-181">System.Int32</span></span>

### <span data-ttu-id="b8c11-182">System.object</span><span class="sxs-lookup"><span data-stu-id="b8c11-182">System.String</span></span>

### <span data-ttu-id="b8c11-183">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="b8c11-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b8c11-184">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c11-184">OUTPUTS</span></span>

### <span data-ttu-id="b8c11-185">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="b8c11-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b8c11-186">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c11-186">NOTES</span></span>

## <span data-ttu-id="b8c11-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c11-187">RELATED LINKS</span></span>

[<span data-ttu-id="b8c11-188">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-189">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-190">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-191">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-192">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-193">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b8c11-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b8c11-194">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b8c11-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
