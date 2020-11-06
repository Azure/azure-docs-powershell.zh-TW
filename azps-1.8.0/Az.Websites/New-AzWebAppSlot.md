---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSlot.md
ms.openlocfilehash: 941de31e1733bd591507176216e30f9e1510f706
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614267"
---
# <span data-ttu-id="57f0d-101">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-101">New-AzWebAppSlot</span></span>

## <span data-ttu-id="57f0d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="57f0d-103">建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="57f0d-103">Creates an Azure Web App slot.</span></span>

## <span data-ttu-id="57f0d-104">句法</span><span class="sxs-lookup"><span data-stu-id="57f0d-104">SYNTAX</span></span>

```
New-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [[-AppServicePlan] <String>]
 [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57f0d-105">說明</span><span class="sxs-lookup"><span data-stu-id="57f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="57f0d-106">**AzWebAppSlot** Cmdlet 會在指定的資源群組中使用指定的應用程式服務方案和資料中心來建立 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="57f0d-106">The **New-AzWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="57f0d-107">示例</span><span class="sxs-lookup"><span data-stu-id="57f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="57f0d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="57f0d-108">Example 1</span></span>
```
PS C:\> New-AzWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="57f0d-109">這個命令會在已有的 Web App 名稱 ContosoSite 中，建立一個名為 Slot001 的槽，在「資料中心」的現有資源群組中的 [預設-網路-WestUS] 西部我們。</span><span class="sxs-lookup"><span data-stu-id="57f0d-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="57f0d-110">此命令使用名為 ContosoServicePlan 的現有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="57f0d-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="57f0d-111">參數</span><span class="sxs-lookup"><span data-stu-id="57f0d-111">PARAMETERS</span></span>

### <span data-ttu-id="57f0d-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="57f0d-112">-AppServicePlan</span></span>
<span data-ttu-id="57f0d-113">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-113">App Service Plan Name</span></span>

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

### <span data-ttu-id="57f0d-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="57f0d-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="57f0d-115">應用程式設定會覆寫 Hashtable</span><span class="sxs-lookup"><span data-stu-id="57f0d-115">App Settings Overrides Hashtable</span></span>

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

### <span data-ttu-id="57f0d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="57f0d-116">-AseName</span></span>
<span data-ttu-id="57f0d-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="57f0d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f0d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="57f0d-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="57f0d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57f0d-120">-AsJob</span></span>
<span data-ttu-id="57f0d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57f0d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57f0d-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="57f0d-122">-ContainerImageName</span></span>
<span data-ttu-id="57f0d-123">容器影像名稱和選用的標籤，例如 (影像： tag) </span><span class="sxs-lookup"><span data-stu-id="57f0d-123">Container Image Name and optional tag, for example (image:tag)</span></span>

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

### <span data-ttu-id="57f0d-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="57f0d-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="57f0d-125">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="57f0d-125">Private Container Registry Password</span></span>

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

### <span data-ttu-id="57f0d-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="57f0d-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="57f0d-127">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="57f0d-127">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="57f0d-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="57f0d-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="57f0d-129">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-129">Private Container Registry Username</span></span>

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

### <span data-ttu-id="57f0d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f0d-130">-DefaultProfile</span></span>
<span data-ttu-id="57f0d-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57f0d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57f0d-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="57f0d-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="57f0d-133">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="57f0d-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="57f0d-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="57f0d-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="57f0d-135">[忽略自訂主機名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="57f0d-135">Ignore Custom HostNames Option</span></span>

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

### <span data-ttu-id="57f0d-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="57f0d-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="57f0d-137">[忽略來源控制] 選項</span><span class="sxs-lookup"><span data-stu-id="57f0d-137">Ignore Source Control Option</span></span>

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

### <span data-ttu-id="57f0d-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-138">-Name</span></span>
<span data-ttu-id="57f0d-139">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-139">Webapp Name</span></span>

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

### <span data-ttu-id="57f0d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f0d-140">-ResourceGroupName</span></span>
<span data-ttu-id="57f0d-141">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-141">Resource Group Name</span></span>

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

### <span data-ttu-id="57f0d-142">-槽</span><span class="sxs-lookup"><span data-stu-id="57f0d-142">-Slot</span></span>
<span data-ttu-id="57f0d-143">Webapp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="57f0d-143">Webapp Slot Name</span></span>

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

### <span data-ttu-id="57f0d-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="57f0d-144">-SourceWebApp</span></span>
<span data-ttu-id="57f0d-145">來源 WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="57f0d-145">Source WebApp Object</span></span>

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

### <span data-ttu-id="57f0d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f0d-146">CommonParameters</span></span>
<span data-ttu-id="57f0d-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57f0d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f0d-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57f0d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f0d-149">輸入</span><span class="sxs-lookup"><span data-stu-id="57f0d-149">INPUTS</span></span>

### <span data-ttu-id="57f0d-150">System.object</span><span class="sxs-lookup"><span data-stu-id="57f0d-150">System.String</span></span>

### <span data-ttu-id="57f0d-151">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="57f0d-151">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57f0d-152">輸出</span><span class="sxs-lookup"><span data-stu-id="57f0d-152">OUTPUTS</span></span>

### <span data-ttu-id="57f0d-153">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="57f0d-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57f0d-154">筆記</span><span class="sxs-lookup"><span data-stu-id="57f0d-154">NOTES</span></span>

## <span data-ttu-id="57f0d-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="57f0d-155">RELATED LINKS</span></span>

[<span data-ttu-id="57f0d-156">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-156">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-157">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-157">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-158">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-158">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-159">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-159">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-160">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-160">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-161">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="57f0d-161">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="57f0d-162">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="57f0d-162">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="57f0d-163">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="57f0d-163">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
