---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614241"
---
# <span data-ttu-id="ab39a-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab39a-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="ab39a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab39a-102">SYNOPSIS</span></span>
<span data-ttu-id="ab39a-103">設定 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="ab39a-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ab39a-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab39a-104">SYNTAX</span></span>

### <span data-ttu-id="ab39a-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab39a-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab39a-106">S2</span><span class="sxs-lookup"><span data-stu-id="ab39a-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab39a-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab39a-107">DESCRIPTION</span></span>
<span data-ttu-id="ab39a-108">**AzAppServicePlan** Cmdlet 會設定 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="ab39a-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="ab39a-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab39a-109">EXAMPLES</span></span>

### <span data-ttu-id="ab39a-110">1：修改 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="ab39a-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="ab39a-111">這個命令會將 PerSiteScaling 選項設定為 true，該應用程式服務方案的名為 ContosoASP，且屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ab39a-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ab39a-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab39a-112">PARAMETERS</span></span>

### <span data-ttu-id="ab39a-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="ab39a-113">-AdminSiteName</span></span>
<span data-ttu-id="ab39a-114">系統管理網站名稱</span><span class="sxs-lookup"><span data-stu-id="ab39a-114">Admin Site Name</span></span>

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

### <span data-ttu-id="ab39a-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ab39a-115">-AppServicePlan</span></span>
<span data-ttu-id="ab39a-116">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="ab39a-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab39a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab39a-117">-AsJob</span></span>
<span data-ttu-id="ab39a-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab39a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab39a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab39a-119">-DefaultProfile</span></span>
<span data-ttu-id="ab39a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab39a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab39a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab39a-121">-Name</span></span>
<span data-ttu-id="ab39a-122">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="ab39a-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab39a-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ab39a-123">-NumberofWorkers</span></span>
<span data-ttu-id="ab39a-124">員工人數</span><span class="sxs-lookup"><span data-stu-id="ab39a-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab39a-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ab39a-125">-PerSiteScaling</span></span>
<span data-ttu-id="ab39a-126">每個網站縮放布林值</span><span class="sxs-lookup"><span data-stu-id="ab39a-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab39a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab39a-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab39a-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ab39a-128">Resource Group Name</span></span>

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

### <span data-ttu-id="ab39a-129">層級</span><span class="sxs-lookup"><span data-stu-id="ab39a-129">-Tier</span></span>
<span data-ttu-id="ab39a-130">端</span><span class="sxs-lookup"><span data-stu-id="ab39a-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab39a-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ab39a-131">-WorkerSize</span></span>
<span data-ttu-id="ab39a-132">工作人員大小</span><span class="sxs-lookup"><span data-stu-id="ab39a-132">Worker Size</span></span>

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

### <span data-ttu-id="ab39a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab39a-133">CommonParameters</span></span>
<span data-ttu-id="ab39a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab39a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab39a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab39a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab39a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ab39a-136">INPUTS</span></span>

### <span data-ttu-id="ab39a-137">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="ab39a-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ab39a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ab39a-138">OUTPUTS</span></span>

### <span data-ttu-id="ab39a-139">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="ab39a-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ab39a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ab39a-140">NOTES</span></span>

## <span data-ttu-id="ab39a-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab39a-141">RELATED LINKS</span></span>

[<span data-ttu-id="ab39a-142">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="ab39a-143">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="ab39a-144">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="ab39a-145">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="ab39a-146">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="ab39a-147">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab39a-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


