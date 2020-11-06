---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454444"
---
# <span data-ttu-id="9931f-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9931f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9931f-102">SYNOPSIS</span></span>
<span data-ttu-id="9931f-103">建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="9931f-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9931f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9931f-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9931f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9931f-105">DESCRIPTION</span></span>
<span data-ttu-id="9931f-106">**AzureRmWebAppSlot** Cmdlet 會在指定的資源群組中使用指定的應用程式服務方案和資料中心來建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="9931f-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="9931f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9931f-107">EXAMPLES</span></span>

### <span data-ttu-id="9931f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9931f-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="9931f-109">這個命令會在已有的 Web App 名稱 ContosoSite 中，建立一個名為 Slot001 的槽，在「資料中心」的現有資源群組中的 [預設-網路-WestUS] 西部我們。</span><span class="sxs-lookup"><span data-stu-id="9931f-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="9931f-110">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="9931f-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="9931f-111">參數</span><span class="sxs-lookup"><span data-stu-id="9931f-111">PARAMETERS</span></span>

### <span data-ttu-id="9931f-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9931f-112">-AppServicePlan</span></span>
<span data-ttu-id="9931f-113">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="9931f-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="9931f-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="9931f-115">應用程式設定會覆寫 Hashtable</span><span class="sxs-lookup"><span data-stu-id="9931f-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9931f-116">-AseName</span></span>
<span data-ttu-id="9931f-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9931f-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9931f-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9931f-120">-AsJob</span></span>
<span data-ttu-id="9931f-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9931f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9931f-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9931f-122">-ContainerImageName</span></span>
<span data-ttu-id="9931f-123">容器影像名稱和選用的標籤，例如 (影像： tag) </span><span class="sxs-lookup"><span data-stu-id="9931f-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="9931f-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9931f-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9931f-125">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="9931f-125">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9931f-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9931f-127">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="9931f-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9931f-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9931f-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="9931f-129">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9931f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9931f-130">-DefaultProfile</span></span>
<span data-ttu-id="9931f-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9931f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9931f-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9931f-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9931f-133">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="9931f-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9931f-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="9931f-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="9931f-135">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="9931f-135">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="9931f-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="9931f-137">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="9931f-137">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-138">-Name</span></span>
<span data-ttu-id="9931f-139">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-139">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9931f-140">-ResourceGroupName</span></span>
<span data-ttu-id="9931f-141">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-141">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-142">-槽</span><span class="sxs-lookup"><span data-stu-id="9931f-142">-Slot</span></span>
<span data-ttu-id="9931f-143">Webapp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="9931f-143">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="9931f-144">-SourceWebApp</span></span>
<span data-ttu-id="9931f-145">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="9931f-145">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9931f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9931f-146">CommonParameters</span></span>
<span data-ttu-id="9931f-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9931f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9931f-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9931f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9931f-149">輸入</span><span class="sxs-lookup"><span data-stu-id="9931f-149">INPUTS</span></span>

### <span data-ttu-id="9931f-150">System.object</span><span class="sxs-lookup"><span data-stu-id="9931f-150">System.String</span></span>

### <span data-ttu-id="9931f-151">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9931f-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9931f-152">參數： SourceWebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9931f-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="9931f-153">輸出</span><span class="sxs-lookup"><span data-stu-id="9931f-153">OUTPUTS</span></span>

### <span data-ttu-id="9931f-154">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9931f-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="9931f-155">筆記</span><span class="sxs-lookup"><span data-stu-id="9931f-155">NOTES</span></span>

## <span data-ttu-id="9931f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="9931f-156">RELATED LINKS</span></span>

[<span data-ttu-id="9931f-157">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-158">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-159">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-161">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-162">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9931f-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9931f-163">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9931f-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="9931f-164">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9931f-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
