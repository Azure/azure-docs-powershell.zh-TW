---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9cadc32a34f94a29221984e25141bcc3a844de4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624525"
---
# <span data-ttu-id="38423-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38423-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="38423-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38423-102">SYNOPSIS</span></span>
<span data-ttu-id="38423-103">在指定的資源群組中取得 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="38423-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38423-104">句法</span><span class="sxs-lookup"><span data-stu-id="38423-104">SYNTAX</span></span>

### <span data-ttu-id="38423-105">S1</span><span class="sxs-lookup"><span data-stu-id="38423-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38423-106">S2</span><span class="sxs-lookup"><span data-stu-id="38423-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38423-107">說明</span><span class="sxs-lookup"><span data-stu-id="38423-107">DESCRIPTION</span></span>
<span data-ttu-id="38423-108">**AzureRmAppServicePlan** Cmdlet 會取得指定資源群組中的 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="38423-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="38423-109">示例</span><span class="sxs-lookup"><span data-stu-id="38423-109">EXAMPLES</span></span>

### <span data-ttu-id="38423-110">範例1：從資源群組取得 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="38423-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="38423-111">這個命令會取得名為 ContosoASP 的應用程式服務方案，這些名稱屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="38423-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="38423-112">範例2：取得位置中的所有 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="38423-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="38423-113">這個命令會取得位於「美國西部」區域中的所有 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="38423-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="38423-114">參數</span><span class="sxs-lookup"><span data-stu-id="38423-114">PARAMETERS</span></span>

### <span data-ttu-id="38423-115">-位置</span><span class="sxs-lookup"><span data-stu-id="38423-115">-Location</span></span>
<span data-ttu-id="38423-116">位於</span><span class="sxs-lookup"><span data-stu-id="38423-116">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38423-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="38423-117">-Name</span></span>
<span data-ttu-id="38423-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="38423-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38423-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38423-119">-ResourceGroupName</span></span>
<span data-ttu-id="38423-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="38423-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38423-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38423-121">-DefaultProfile</span></span>
<span data-ttu-id="38423-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38423-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38423-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38423-123">CommonParameters</span></span>
<span data-ttu-id="38423-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38423-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38423-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38423-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38423-126">輸入</span><span class="sxs-lookup"><span data-stu-id="38423-126">INPUTS</span></span>

## <span data-ttu-id="38423-127">輸出</span><span class="sxs-lookup"><span data-stu-id="38423-127">OUTPUTS</span></span>

### <span data-ttu-id="38423-128">ServerFarmWithRichSku 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="38423-128">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="38423-129">ServerFarmCollection 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="38423-129">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="38423-130">筆記</span><span class="sxs-lookup"><span data-stu-id="38423-130">NOTES</span></span>

## <span data-ttu-id="38423-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="38423-131">RELATED LINKS</span></span>

[<span data-ttu-id="38423-132">新-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38423-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="38423-133">移除-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38423-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="38423-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="38423-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


