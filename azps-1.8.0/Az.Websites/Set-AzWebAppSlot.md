---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614235"
---
# <span data-ttu-id="a386e-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="a386e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a386e-102">SYNOPSIS</span></span>
<span data-ttu-id="a386e-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="a386e-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="a386e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a386e-104">SYNTAX</span></span>

### <span data-ttu-id="a386e-105">S1</span><span class="sxs-lookup"><span data-stu-id="a386e-105">S1</span></span>
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

### <span data-ttu-id="a386e-106">S2</span><span class="sxs-lookup"><span data-stu-id="a386e-106">S2</span></span>
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

## <span data-ttu-id="a386e-107">說明</span><span class="sxs-lookup"><span data-stu-id="a386e-107">DESCRIPTION</span></span>
<span data-ttu-id="a386e-108">**AzWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="a386e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="a386e-109">示例</span><span class="sxs-lookup"><span data-stu-id="a386e-109">EXAMPLES</span></span>

### <span data-ttu-id="a386e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a386e-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="a386e-111">這個命令會變更與 Slot001 相關聯的 appservice 方案（與資源群組預設-Web-WestUS 相關的 Webapp ContosoWebApp）。</span><span class="sxs-lookup"><span data-stu-id="a386e-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a386e-112">使用連結 learm 變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="a386e-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="a386e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="a386e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="a386e-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a386e-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="a386e-115">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="a386e-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="a386e-116">參數</span><span class="sxs-lookup"><span data-stu-id="a386e-116">PARAMETERS</span></span>

### <span data-ttu-id="a386e-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a386e-117">-AppServicePlan</span></span>
<span data-ttu-id="a386e-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="a386e-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a386e-119">-AppSettings</span></span>
<span data-ttu-id="a386e-120">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="a386e-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="a386e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a386e-121">-AsJob</span></span>
<span data-ttu-id="a386e-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a386e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a386e-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a386e-123">-AssignIdentity</span></span>
<span data-ttu-id="a386e-124">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="a386e-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="a386e-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a386e-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="a386e-126">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="a386e-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a386e-127">-AzureStoragePath</span></span>
<span data-ttu-id="a386e-128">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="a386e-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="a386e-129">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="a386e-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="a386e-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a386e-130">-ConnectionStrings</span></span>
<span data-ttu-id="a386e-131">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="a386e-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="a386e-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a386e-132">-ContainerImageName</span></span>
<span data-ttu-id="a386e-133">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-133">Container Image Name</span></span>

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

### <span data-ttu-id="a386e-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a386e-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="a386e-135">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="a386e-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="a386e-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a386e-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="a386e-137">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="a386e-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="a386e-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a386e-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="a386e-139">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="a386e-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a386e-140">-DefaultDocuments</span></span>
<span data-ttu-id="a386e-141">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="a386e-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="a386e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a386e-142">-DefaultProfile</span></span>
<span data-ttu-id="a386e-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a386e-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a386e-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a386e-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="a386e-145">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="a386e-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="a386e-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a386e-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="a386e-147">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="a386e-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="a386e-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a386e-148">-HandlerMappings</span></span>
<span data-ttu-id="a386e-149">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="a386e-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="a386e-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a386e-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="a386e-151">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="a386e-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="a386e-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a386e-152">-HttpsOnly</span></span>
<span data-ttu-id="a386e-153">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="a386e-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="a386e-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a386e-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="a386e-155">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="a386e-156">-名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-156">-Name</span></span>
<span data-ttu-id="a386e-157">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-157">WebApp Name</span></span>

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

### <span data-ttu-id="a386e-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a386e-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="a386e-159">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="a386e-159">Net Framework Version</span></span>

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

### <span data-ttu-id="a386e-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a386e-160">-NumberOfWorkers</span></span>
<span data-ttu-id="a386e-161">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="a386e-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="a386e-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a386e-162">-PhpVersion</span></span>
<span data-ttu-id="a386e-163">Php 版本</span><span class="sxs-lookup"><span data-stu-id="a386e-163">Php Version</span></span>

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

### <span data-ttu-id="a386e-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a386e-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="a386e-165">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="a386e-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="a386e-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a386e-166">-ResourceGroupName</span></span>
<span data-ttu-id="a386e-167">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-167">Resource Group Name</span></span>

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

### <span data-ttu-id="a386e-168">-槽</span><span class="sxs-lookup"><span data-stu-id="a386e-168">-Slot</span></span>
<span data-ttu-id="a386e-169">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="a386e-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a386e-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a386e-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="a386e-171">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="a386e-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="a386e-172">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a386e-172">-WebApp</span></span>
<span data-ttu-id="a386e-173">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="a386e-173">WebApp Object</span></span>

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

### <span data-ttu-id="a386e-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a386e-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="a386e-175">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="a386e-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="a386e-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a386e-176">CommonParameters</span></span>
<span data-ttu-id="a386e-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a386e-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a386e-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a386e-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a386e-179">輸入</span><span class="sxs-lookup"><span data-stu-id="a386e-179">INPUTS</span></span>

### <span data-ttu-id="a386e-180">System.object</span><span class="sxs-lookup"><span data-stu-id="a386e-180">System.Int32</span></span>

### <span data-ttu-id="a386e-181">System.object</span><span class="sxs-lookup"><span data-stu-id="a386e-181">System.String</span></span>

### <span data-ttu-id="a386e-182">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a386e-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a386e-183">輸出</span><span class="sxs-lookup"><span data-stu-id="a386e-183">OUTPUTS</span></span>

### <span data-ttu-id="a386e-184">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a386e-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a386e-185">筆記</span><span class="sxs-lookup"><span data-stu-id="a386e-185">NOTES</span></span>

## <span data-ttu-id="a386e-186">相關連結</span><span class="sxs-lookup"><span data-stu-id="a386e-186">RELATED LINKS</span></span>

[<span data-ttu-id="a386e-187">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a386e-188">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="a386e-189">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="a386e-190">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="a386e-191">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="a386e-192">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a386e-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="a386e-193">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a386e-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
