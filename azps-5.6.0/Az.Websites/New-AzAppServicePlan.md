---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916817"
---
# <span data-ttu-id="ad51f-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="ad51f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad51f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad51f-103">在指定地理位置建立 Azure 應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="ad51f-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="ad51f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad51f-104">SYNTAX</span></span>

### <span data-ttu-id="ad51f-105">S1</span><span class="sxs-lookup"><span data-stu-id="ad51f-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad51f-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad51f-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad51f-107">描述</span><span class="sxs-lookup"><span data-stu-id="ad51f-107">DESCRIPTION</span></span>
<span data-ttu-id="ad51f-108">**New-AzAppServicePlan** Cmdlet 會以指定的層級、員工大小和員工人數，在指定的地理位置建立 Azure 應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="ad51f-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="ad51f-109">例子</span><span class="sxs-lookup"><span data-stu-id="ad51f-109">EXAMPLES</span></span>

### <span data-ttu-id="ad51f-110">範例 1：建立應用程式服務計畫</span><span class="sxs-lookup"><span data-stu-id="ad51f-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="ad51f-111">此命令會在美國西部地理位置名為 Default-Web-WestUS 的資源群組中，建立名為 ContosoASP 的應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="ad51f-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="ad51f-112">命令會指定基本層級，並配置兩位小型工作者。</span><span class="sxs-lookup"><span data-stu-id="ad51f-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="ad51f-113">參數</span><span class="sxs-lookup"><span data-stu-id="ad51f-113">PARAMETERS</span></span>

### <span data-ttu-id="ad51f-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-114">-AppServicePlan</span></span>
<span data-ttu-id="ad51f-115">應用程式服務計畫物件</span><span class="sxs-lookup"><span data-stu-id="ad51f-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="ad51f-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="ad51f-116">-AseName</span></span>
<span data-ttu-id="ad51f-117">應用程式服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="ad51f-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="ad51f-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad51f-118">-AseResourceGroupName</span></span>
<span data-ttu-id="ad51f-119">應用程式服務環境資源組名</span><span class="sxs-lookup"><span data-stu-id="ad51f-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="ad51f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad51f-120">-AsJob</span></span>
<span data-ttu-id="ad51f-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad51f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad51f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad51f-122">-DefaultProfile</span></span>
<span data-ttu-id="ad51f-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad51f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad51f-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="ad51f-124">-HyperV</span></span>
<span data-ttu-id="ad51f-125">指定此，應用程式服務計畫會執行 Windows 容器</span><span class="sxs-lookup"><span data-stu-id="ad51f-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="ad51f-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="ad51f-126">-Linux</span></span>
<span data-ttu-id="ad51f-127">指定此，應用程式服務計畫會執行 Linux 容器</span><span class="sxs-lookup"><span data-stu-id="ad51f-127">Specify this, App Service Plan will run Linux Containers</span></span>

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

### <span data-ttu-id="ad51f-128">-位置</span><span class="sxs-lookup"><span data-stu-id="ad51f-128">-Location</span></span>
<span data-ttu-id="ad51f-129">位置</span><span class="sxs-lookup"><span data-stu-id="ad51f-129">Location</span></span> 

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

### <span data-ttu-id="ad51f-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad51f-130">-Name</span></span>
<span data-ttu-id="ad51f-131">應用程式服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="ad51f-131">App Service Plan Name</span></span>

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

### <span data-ttu-id="ad51f-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="ad51f-132">-NumberofWorkers</span></span>
<span data-ttu-id="ad51f-133">工作人員人數</span><span class="sxs-lookup"><span data-stu-id="ad51f-133">Number Of Workers</span></span>

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

### <span data-ttu-id="ad51f-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="ad51f-134">-PerSiteScaling</span></span>
<span data-ttu-id="ad51f-135">是否要啟用每個網站縮放比例</span><span class="sxs-lookup"><span data-stu-id="ad51f-135">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="ad51f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad51f-136">-ResourceGroupName</span></span>
<span data-ttu-id="ad51f-137">資源組名</span><span class="sxs-lookup"><span data-stu-id="ad51f-137">Resource Group Name</span></span>

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

### <span data-ttu-id="ad51f-138">-標記</span><span class="sxs-lookup"><span data-stu-id="ad51f-138">-Tag</span></span>
<span data-ttu-id="ad51f-139">標記是名稱/值組，可讓您將資源分類</span><span class="sxs-lookup"><span data-stu-id="ad51f-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad51f-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="ad51f-140">-Tier</span></span>
<span data-ttu-id="ad51f-141">層</span><span class="sxs-lookup"><span data-stu-id="ad51f-141">Tier</span></span>

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

### <span data-ttu-id="ad51f-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="ad51f-142">-WorkerSize</span></span>
<span data-ttu-id="ad51f-143">網頁工作者的大小</span><span class="sxs-lookup"><span data-stu-id="ad51f-143">Size of web worker</span></span>

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

### <span data-ttu-id="ad51f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad51f-144">CommonParameters</span></span>
<span data-ttu-id="ad51f-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad51f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad51f-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad51f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad51f-147">輸入</span><span class="sxs-lookup"><span data-stu-id="ad51f-147">INPUTS</span></span>

### <span data-ttu-id="ad51f-148">Microsoft.Azure.Commands.WebApps.models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ad51f-149">輸出</span><span class="sxs-lookup"><span data-stu-id="ad51f-149">OUTPUTS</span></span>

### <span data-ttu-id="ad51f-150">Microsoft.Azure.Commands.WebApps.models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="ad51f-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ad51f-151">NOTES</span></span>

## <span data-ttu-id="ad51f-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad51f-152">RELATED LINKS</span></span>

[<span data-ttu-id="ad51f-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="ad51f-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="ad51f-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ad51f-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


