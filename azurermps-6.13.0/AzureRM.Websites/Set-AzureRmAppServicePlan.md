---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449651"
---
# <span data-ttu-id="de06c-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de06c-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="de06c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de06c-102">SYNOPSIS</span></span>
<span data-ttu-id="de06c-103">設定 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="de06c-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de06c-104">句法</span><span class="sxs-lookup"><span data-stu-id="de06c-104">SYNTAX</span></span>

### <span data-ttu-id="de06c-105">S1</span><span class="sxs-lookup"><span data-stu-id="de06c-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de06c-106">S2</span><span class="sxs-lookup"><span data-stu-id="de06c-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de06c-107">說明</span><span class="sxs-lookup"><span data-stu-id="de06c-107">DESCRIPTION</span></span>
<span data-ttu-id="de06c-108">**AzureRmAppServicePlan** Cmdlet 會設定 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="de06c-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="de06c-109">示例</span><span class="sxs-lookup"><span data-stu-id="de06c-109">EXAMPLES</span></span>

### <span data-ttu-id="de06c-110">1：修改 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="de06c-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="de06c-111">這個命令會將 PerSiteScaling 選項設定為 true，該應用程式服務方案的名為 ContosoASP，且屬於名為 [預設-Web-WestUS] 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="de06c-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="de06c-112">參數</span><span class="sxs-lookup"><span data-stu-id="de06c-112">PARAMETERS</span></span>

### <span data-ttu-id="de06c-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="de06c-113">-AdminSiteName</span></span>
<span data-ttu-id="de06c-114">系統管理網站名稱</span><span class="sxs-lookup"><span data-stu-id="de06c-114">Admin Site Name</span></span>

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

### <span data-ttu-id="de06c-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="de06c-115">-AppServicePlan</span></span>
<span data-ttu-id="de06c-116">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="de06c-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="de06c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de06c-117">-AsJob</span></span>
<span data-ttu-id="de06c-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="de06c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de06c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de06c-119">-DefaultProfile</span></span>
<span data-ttu-id="de06c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de06c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de06c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="de06c-121">-Name</span></span>
<span data-ttu-id="de06c-122">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="de06c-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="de06c-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="de06c-123">-NumberofWorkers</span></span>
<span data-ttu-id="de06c-124">員工人數</span><span class="sxs-lookup"><span data-stu-id="de06c-124">Number Of Workers</span></span>

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

### <span data-ttu-id="de06c-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="de06c-125">-PerSiteScaling</span></span>
<span data-ttu-id="de06c-126">每個網站縮放布林值</span><span class="sxs-lookup"><span data-stu-id="de06c-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="de06c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de06c-127">-ResourceGroupName</span></span>
<span data-ttu-id="de06c-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="de06c-128">Resource Group Name</span></span>

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

### <span data-ttu-id="de06c-129">層級</span><span class="sxs-lookup"><span data-stu-id="de06c-129">-Tier</span></span>
<span data-ttu-id="de06c-130">端</span><span class="sxs-lookup"><span data-stu-id="de06c-130">Tier</span></span>

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

### <span data-ttu-id="de06c-131">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="de06c-131">-WorkerSize</span></span>
<span data-ttu-id="de06c-132">工作人員大小</span><span class="sxs-lookup"><span data-stu-id="de06c-132">Worker Size</span></span>

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

### <span data-ttu-id="de06c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de06c-133">CommonParameters</span></span>
<span data-ttu-id="de06c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de06c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de06c-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de06c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de06c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="de06c-136">INPUTS</span></span>

### <span data-ttu-id="de06c-137">AppServicePlan 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="de06c-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="de06c-138">參數： AppServicePlan (ByValue) </span><span class="sxs-lookup"><span data-stu-id="de06c-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="de06c-139">輸出</span><span class="sxs-lookup"><span data-stu-id="de06c-139">OUTPUTS</span></span>

### <span data-ttu-id="de06c-140">AppServicePlan 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="de06c-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="de06c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="de06c-141">NOTES</span></span>

## <span data-ttu-id="de06c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="de06c-142">RELATED LINKS</span></span>

[<span data-ttu-id="de06c-143">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="de06c-144">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="de06c-145">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="de06c-146">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="de06c-147">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="de06c-148">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de06c-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


