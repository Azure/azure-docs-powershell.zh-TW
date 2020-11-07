---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09491e82a1eb0ab6b77a382fc727d385bbd6820f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625384"
---
# <span data-ttu-id="5ddda-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ddda-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="5ddda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ddda-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddda-103">在指定的地理位置建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="5ddda-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ddda-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ddda-104">SYNTAX</span></span>

### <span data-ttu-id="5ddda-105">S1</span><span class="sxs-lookup"><span data-stu-id="5ddda-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ddda-106">S2</span><span class="sxs-lookup"><span data-stu-id="5ddda-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ddda-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ddda-107">DESCRIPTION</span></span>
<span data-ttu-id="5ddda-108">**新的 AzureRmAppServicePlan** Cmdlet 會在指定的地理位置中使用指定的層級、輔助角色大小及工作人員數量來建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="5ddda-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="5ddda-109">示例</span><span class="sxs-lookup"><span data-stu-id="5ddda-109">EXAMPLES</span></span>

### <span data-ttu-id="5ddda-110">範例1：建立應用程式服務方案</span><span class="sxs-lookup"><span data-stu-id="5ddda-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="5ddda-111">這個命令會在名為 ContosoASP 的資源群組中建立名為的應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="5ddda-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="5ddda-112">此命令會指定基本的層級，並會分配兩個小型工作人員。</span><span class="sxs-lookup"><span data-stu-id="5ddda-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="5ddda-113">參數</span><span class="sxs-lookup"><span data-stu-id="5ddda-113">PARAMETERS</span></span>

### <span data-ttu-id="5ddda-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ddda-114">-AppServicePlan</span></span>
<span data-ttu-id="5ddda-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="5ddda-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="5ddda-116">-AseName</span></span>
<span data-ttu-id="5ddda-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="5ddda-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="5ddda-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddda-118">-AseResourceGroupName</span></span>
<span data-ttu-id="5ddda-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5ddda-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddda-120">-DefaultProfile</span></span>
<span data-ttu-id="5ddda-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ddda-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ddda-122">-位置</span><span class="sxs-lookup"><span data-stu-id="5ddda-122">-Location</span></span>
<span data-ttu-id="5ddda-123">位於</span><span class="sxs-lookup"><span data-stu-id="5ddda-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ddda-124">-Name</span></span>
<span data-ttu-id="5ddda-125">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="5ddda-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="5ddda-126">-NumberofWorkers</span></span>
<span data-ttu-id="5ddda-127">員工人數</span><span class="sxs-lookup"><span data-stu-id="5ddda-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="5ddda-128">-PerSiteScaling</span></span>
<span data-ttu-id="5ddda-129">是否要啟用每個網站縮放比例</span><span class="sxs-lookup"><span data-stu-id="5ddda-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddda-130">-ResourceGroupName</span></span>
<span data-ttu-id="5ddda-131">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5ddda-131">Resource Group Name</span></span>

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

### <span data-ttu-id="5ddda-132">層級</span><span class="sxs-lookup"><span data-stu-id="5ddda-132">-Tier</span></span>
<span data-ttu-id="5ddda-133">端</span><span class="sxs-lookup"><span data-stu-id="5ddda-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddda-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="5ddda-134">-WorkerSize</span></span>
<span data-ttu-id="5ddda-135">網頁 worker 的大小</span><span class="sxs-lookup"><span data-stu-id="5ddda-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="5ddda-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ddda-136">-AsJob</span></span>
<span data-ttu-id="5ddda-137">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5ddda-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ddda-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddda-138">CommonParameters</span></span>
<span data-ttu-id="5ddda-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ddda-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddda-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ddda-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddda-141">輸入</span><span class="sxs-lookup"><span data-stu-id="5ddda-141">INPUTS</span></span>

### <span data-ttu-id="5ddda-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="5ddda-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="5ddda-143">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="5ddda-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="5ddda-144">輸出</span><span class="sxs-lookup"><span data-stu-id="5ddda-144">OUTPUTS</span></span>

### <span data-ttu-id="5ddda-145">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="5ddda-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="5ddda-146">筆記</span><span class="sxs-lookup"><span data-stu-id="5ddda-146">NOTES</span></span>

## <span data-ttu-id="5ddda-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ddda-147">RELATED LINKS</span></span>

[<span data-ttu-id="5ddda-148">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ddda-148">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5ddda-149">移除-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ddda-149">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="5ddda-150">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5ddda-150">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


