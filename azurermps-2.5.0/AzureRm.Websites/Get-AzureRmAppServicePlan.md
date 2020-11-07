---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800273"
---
# <span data-ttu-id="9d736-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9d736-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9d736-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d736-102">SYNOPSIS</span></span>
<span data-ttu-id="9d736-103">在指定的資源群組中取得 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="9d736-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d736-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d736-104">SYNTAX</span></span>

### <span data-ttu-id="9d736-105">S1</span><span class="sxs-lookup"><span data-stu-id="9d736-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d736-106">S2</span><span class="sxs-lookup"><span data-stu-id="9d736-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d736-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d736-107">DESCRIPTION</span></span>
<span data-ttu-id="9d736-108">**AzureRmAppServicePlan** Cmdlet 會取得指定資源群組中的 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="9d736-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="9d736-109">示例</span><span class="sxs-lookup"><span data-stu-id="9d736-109">EXAMPLES</span></span>

### <span data-ttu-id="9d736-110">範例1：從資源群組取得 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="9d736-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="9d736-111">這個命令會取得名為 ContosoASP 的應用程式服務方案，這些名稱屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9d736-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="9d736-112">範例2：取得位置中的所有 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="9d736-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="9d736-113">這個命令會取得位於「美國西部」區域中的所有 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="9d736-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="9d736-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d736-114">PARAMETERS</span></span>

### <span data-ttu-id="9d736-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d736-115">-DefaultProfile</span></span>
<span data-ttu-id="9d736-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d736-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d736-117">-位置</span><span class="sxs-lookup"><span data-stu-id="9d736-117">-Location</span></span>
<span data-ttu-id="9d736-118">位於</span><span class="sxs-lookup"><span data-stu-id="9d736-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d736-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d736-119">-Name</span></span>
<span data-ttu-id="9d736-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="9d736-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d736-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d736-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d736-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9d736-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d736-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d736-123">CommonParameters</span></span>
<span data-ttu-id="9d736-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d736-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d736-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d736-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d736-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9d736-126">INPUTS</span></span>

### <span data-ttu-id="9d736-127">所有</span><span class="sxs-lookup"><span data-stu-id="9d736-127">None</span></span>
<span data-ttu-id="9d736-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9d736-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d736-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9d736-129">OUTPUTS</span></span>

### <span data-ttu-id="9d736-130">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="9d736-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="9d736-131">ServerFarmCollection 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="9d736-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="9d736-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9d736-132">NOTES</span></span>

## <span data-ttu-id="9d736-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d736-133">RELATED LINKS</span></span>

[<span data-ttu-id="9d736-134">新-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9d736-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="9d736-135">移除-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9d736-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="9d736-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9d736-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


