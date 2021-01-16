---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: af94f1bec48bf54284ccf6e0011753a737dac30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436008"
---
# <span data-ttu-id="fdd1d-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fdd1d-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="fdd1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdd1d-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd1d-103">在指定的地理位置建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="fdd1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdd1d-104">SYNTAX</span></span>

### <span data-ttu-id="fdd1d-105">S1</span><span class="sxs-lookup"><span data-stu-id="fdd1d-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdd1d-106">S2</span><span class="sxs-lookup"><span data-stu-id="fdd1d-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdd1d-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdd1d-107">DESCRIPTION</span></span>
<span data-ttu-id="fdd1d-108">**新的 AzAppServicePlan** Cmdlet 會在指定的地理位置中使用指定的層級、輔助角色大小及工作人員數量來建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="fdd1d-109">示例</span><span class="sxs-lookup"><span data-stu-id="fdd1d-109">EXAMPLES</span></span>

### <span data-ttu-id="fdd1d-110">範例1：建立應用程式服務方案</span><span class="sxs-lookup"><span data-stu-id="fdd1d-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="fdd1d-111">這個命令會在名為 ContosoASP 的資源群組中建立名為的應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="fdd1d-112">此命令會指定基本的層級，並會分配兩個小型工作人員。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="fdd1d-113">參數</span><span class="sxs-lookup"><span data-stu-id="fdd1d-113">PARAMETERS</span></span>

### <span data-ttu-id="fdd1d-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fdd1d-114">-AppServicePlan</span></span>
<span data-ttu-id="fdd1d-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="fdd1d-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="fdd1d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="fdd1d-116">-AseName</span></span>
<span data-ttu-id="fdd1d-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="fdd1d-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="fdd1d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd1d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="fdd1d-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fdd1d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdd1d-120">-AsJob</span></span>
<span data-ttu-id="fdd1d-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fdd1d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdd1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd1d-122">-DefaultProfile</span></span>
<span data-ttu-id="fdd1d-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdd1d-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="fdd1d-124">-HyperV</span></span>
<span data-ttu-id="fdd1d-125">指定這個，應用程式服務計畫將會執行 Windows 容器</span><span class="sxs-lookup"><span data-stu-id="fdd1d-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-126">-位置</span><span class="sxs-lookup"><span data-stu-id="fdd1d-126">-Location</span></span>
<span data-ttu-id="fdd1d-127">位於</span><span class="sxs-lookup"><span data-stu-id="fdd1d-127">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdd1d-128">-Name</span></span>
<span data-ttu-id="fdd1d-129">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="fdd1d-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="fdd1d-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="fdd1d-130">-NumberofWorkers</span></span>
<span data-ttu-id="fdd1d-131">員工人數</span><span class="sxs-lookup"><span data-stu-id="fdd1d-131">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="fdd1d-132">-PerSiteScaling</span></span>
<span data-ttu-id="fdd1d-133">是否要啟用每個網站縮放比例</span><span class="sxs-lookup"><span data-stu-id="fdd1d-133">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd1d-134">-ResourceGroupName</span></span>
<span data-ttu-id="fdd1d-135">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fdd1d-135">Resource Group Name</span></span>

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

### <span data-ttu-id="fdd1d-136">層級</span><span class="sxs-lookup"><span data-stu-id="fdd1d-136">-Tier</span></span>
<span data-ttu-id="fdd1d-137">端</span><span class="sxs-lookup"><span data-stu-id="fdd1d-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="fdd1d-138">-WorkerSize</span></span>
<span data-ttu-id="fdd1d-139">網頁 worker 的大小</span><span class="sxs-lookup"><span data-stu-id="fdd1d-139">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd1d-140">CommonParameters</span></span>
<span data-ttu-id="fdd1d-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd1d-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdd1d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd1d-143">輸入</span><span class="sxs-lookup"><span data-stu-id="fdd1d-143">INPUTS</span></span>

### <span data-ttu-id="fdd1d-144">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="fdd1d-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="fdd1d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="fdd1d-145">OUTPUTS</span></span>

### <span data-ttu-id="fdd1d-146">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="fdd1d-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="fdd1d-147">筆記</span><span class="sxs-lookup"><span data-stu-id="fdd1d-147">NOTES</span></span>

## <span data-ttu-id="fdd1d-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdd1d-148">RELATED LINKS</span></span>

[<span data-ttu-id="fdd1d-149">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fdd1d-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="fdd1d-150">移除-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fdd1d-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="fdd1d-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fdd1d-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


