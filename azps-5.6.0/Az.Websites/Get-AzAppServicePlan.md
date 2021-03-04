---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: bbe4cf87c3af86cd8a4e72f239d4aca7c3386786
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909262"
---
# <span data-ttu-id="fb6ec-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb6ec-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="fb6ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6ec-103">在指定的資源群組中，獲得 Azure 應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="fb6ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb6ec-104">SYNTAX</span></span>

### <span data-ttu-id="fb6ec-105">S1</span><span class="sxs-lookup"><span data-stu-id="fb6ec-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb6ec-106">S2</span><span class="sxs-lookup"><span data-stu-id="fb6ec-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb6ec-107">描述</span><span class="sxs-lookup"><span data-stu-id="fb6ec-107">DESCRIPTION</span></span>
<span data-ttu-id="fb6ec-108">**Get-AzAppServicePlan** Cmdlet 會取得指定資源群組中的 Azure 應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="fb6ec-109">例子</span><span class="sxs-lookup"><span data-stu-id="fb6ec-109">EXAMPLES</span></span>

### <span data-ttu-id="fb6ec-110">範例 1：從資源群組取得應用程式服務計畫</span><span class="sxs-lookup"><span data-stu-id="fb6ec-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="fb6ec-111">此命令會獲得名為 ContosoASP 的應用程式服務計畫，該計畫屬於 Default-Web-WestUS 資源群組。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="fb6ec-112">範例 2：在位置中取得所有應用程式服務方案</span><span class="sxs-lookup"><span data-stu-id="fb6ec-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="fb6ec-113">此命令會獲得位於「美國西部」地區的所有應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="fb6ec-114">參數</span><span class="sxs-lookup"><span data-stu-id="fb6ec-114">PARAMETERS</span></span>

### <span data-ttu-id="fb6ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6ec-115">-DefaultProfile</span></span>
<span data-ttu-id="fb6ec-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb6ec-117">-位置</span><span class="sxs-lookup"><span data-stu-id="fb6ec-117">-Location</span></span>
<span data-ttu-id="fb6ec-118">位置</span><span class="sxs-lookup"><span data-stu-id="fb6ec-118">Location</span></span> 

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

### <span data-ttu-id="fb6ec-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb6ec-119">-Name</span></span>
<span data-ttu-id="fb6ec-120">應用程式服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="fb6ec-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="fb6ec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6ec-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb6ec-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="fb6ec-122">Resource Group Name</span></span>

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

### <span data-ttu-id="fb6ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6ec-123">CommonParameters</span></span>
<span data-ttu-id="fb6ec-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6ec-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb6ec-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6ec-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fb6ec-126">INPUTS</span></span>

### <span data-ttu-id="fb6ec-127">沒有</span><span class="sxs-lookup"><span data-stu-id="fb6ec-127">None</span></span>

## <span data-ttu-id="fb6ec-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fb6ec-128">OUTPUTS</span></span>

### <span data-ttu-id="fb6ec-129">Microsoft.Azure.Commands.WebApps.models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb6ec-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="fb6ec-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fb6ec-130">NOTES</span></span>

## <span data-ttu-id="fb6ec-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb6ec-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb6ec-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb6ec-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="fb6ec-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb6ec-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="fb6ec-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="fb6ec-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


