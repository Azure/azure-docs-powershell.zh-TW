---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625947"
---
# <span data-ttu-id="8c840-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c840-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="8c840-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c840-102">SYNOPSIS</span></span>
<span data-ttu-id="8c840-103">在指定的地理位置建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="8c840-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c840-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c840-104">SYNTAX</span></span>

### <span data-ttu-id="8c840-105">S1</span><span class="sxs-lookup"><span data-stu-id="8c840-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c840-106">S2</span><span class="sxs-lookup"><span data-stu-id="8c840-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c840-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c840-107">DESCRIPTION</span></span>
<span data-ttu-id="8c840-108">**新的 AzureRmAppServicePlan** Cmdlet 會在指定的地理位置中使用指定的層級、輔助角色大小及工作人員數量來建立 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="8c840-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="8c840-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c840-109">EXAMPLES</span></span>

### <span data-ttu-id="8c840-110">範例1：建立應用程式服務方案</span><span class="sxs-lookup"><span data-stu-id="8c840-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="8c840-111">這個命令會在名為 ContosoASP 的資源群組中建立名為的應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="8c840-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="8c840-112">此命令會指定基本的層級，並會分配兩個小型工作人員。</span><span class="sxs-lookup"><span data-stu-id="8c840-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="8c840-113">參數</span><span class="sxs-lookup"><span data-stu-id="8c840-113">PARAMETERS</span></span>

### <span data-ttu-id="8c840-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c840-114">-AppServicePlan</span></span>
<span data-ttu-id="8c840-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="8c840-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c840-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="8c840-116">-AseName</span></span>
<span data-ttu-id="8c840-117">App 服務環境名稱</span><span class="sxs-lookup"><span data-stu-id="8c840-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="8c840-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c840-118">-AseResourceGroupName</span></span>
<span data-ttu-id="8c840-119">App 服務環境資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8c840-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="8c840-120">-位置</span><span class="sxs-lookup"><span data-stu-id="8c840-120">-Location</span></span>
<span data-ttu-id="8c840-121">位於</span><span class="sxs-lookup"><span data-stu-id="8c840-121">Location</span></span> 

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

### <span data-ttu-id="8c840-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c840-122">-Name</span></span>
<span data-ttu-id="8c840-123">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="8c840-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="8c840-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="8c840-124">-NumberofWorkers</span></span>
<span data-ttu-id="8c840-125">員工人數</span><span class="sxs-lookup"><span data-stu-id="8c840-125">Number Of Workers</span></span>

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

### <span data-ttu-id="8c840-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="8c840-126">-PerSiteScaling</span></span>
<span data-ttu-id="8c840-127">是否要啟用每個網站縮放比例</span><span class="sxs-lookup"><span data-stu-id="8c840-127">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="8c840-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c840-128">-ResourceGroupName</span></span>
<span data-ttu-id="8c840-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8c840-129">Resource Group Name</span></span>

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

### <span data-ttu-id="8c840-130">層級</span><span class="sxs-lookup"><span data-stu-id="8c840-130">-Tier</span></span>
<span data-ttu-id="8c840-131">端</span><span class="sxs-lookup"><span data-stu-id="8c840-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c840-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="8c840-132">-WorkerSize</span></span>
<span data-ttu-id="8c840-133">網頁 worker 的大小</span><span class="sxs-lookup"><span data-stu-id="8c840-133">Size of web worker</span></span>

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

### <span data-ttu-id="8c840-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c840-134">-DefaultProfile</span></span>
<span data-ttu-id="8c840-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c840-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c840-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c840-136">CommonParameters</span></span>
<span data-ttu-id="8c840-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c840-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c840-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c840-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c840-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8c840-139">INPUTS</span></span>

### <span data-ttu-id="8c840-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8c840-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="8c840-141">形參 "AppServicePlan" 接受管線中 "ServerFarmWithRichSku" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8c840-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="8c840-142">輸出</span><span class="sxs-lookup"><span data-stu-id="8c840-142">OUTPUTS</span></span>

### <span data-ttu-id="8c840-143">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="8c840-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="8c840-144">筆記</span><span class="sxs-lookup"><span data-stu-id="8c840-144">NOTES</span></span>

## <span data-ttu-id="8c840-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c840-145">RELATED LINKS</span></span>

[<span data-ttu-id="8c840-146">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c840-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="8c840-147">移除-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c840-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="8c840-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8c840-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


