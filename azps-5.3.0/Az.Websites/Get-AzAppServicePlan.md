---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287383"
---
# <span data-ttu-id="67455-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67455-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="67455-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67455-102">SYNOPSIS</span></span>
<span data-ttu-id="67455-103">在指定的資源群組中取得 Azure App Service 方案。</span><span class="sxs-lookup"><span data-stu-id="67455-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="67455-104">句法</span><span class="sxs-lookup"><span data-stu-id="67455-104">SYNTAX</span></span>

### <span data-ttu-id="67455-105">S1</span><span class="sxs-lookup"><span data-stu-id="67455-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67455-106">S2</span><span class="sxs-lookup"><span data-stu-id="67455-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67455-107">說明</span><span class="sxs-lookup"><span data-stu-id="67455-107">DESCRIPTION</span></span>
<span data-ttu-id="67455-108">**AzAppServicePlan** Cmdlet 會取得指定資源群組中的 Azure App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="67455-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="67455-109">示例</span><span class="sxs-lookup"><span data-stu-id="67455-109">EXAMPLES</span></span>

### <span data-ttu-id="67455-110">範例1：從資源群組取得 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="67455-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="67455-111">這個命令會取得名為 ContosoASP 的應用程式服務方案，這些名稱屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="67455-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="67455-112">範例2：取得位置中的所有 App 服務方案</span><span class="sxs-lookup"><span data-stu-id="67455-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="67455-113">這個命令會取得位於「美國西部」區域中的所有 App 服務方案。</span><span class="sxs-lookup"><span data-stu-id="67455-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="67455-114">參數</span><span class="sxs-lookup"><span data-stu-id="67455-114">PARAMETERS</span></span>

### <span data-ttu-id="67455-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67455-115">-DefaultProfile</span></span>
<span data-ttu-id="67455-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67455-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67455-117">-位置</span><span class="sxs-lookup"><span data-stu-id="67455-117">-Location</span></span>
<span data-ttu-id="67455-118">位於</span><span class="sxs-lookup"><span data-stu-id="67455-118">Location</span></span> 

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

### <span data-ttu-id="67455-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="67455-119">-Name</span></span>
<span data-ttu-id="67455-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="67455-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="67455-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67455-121">-ResourceGroupName</span></span>
<span data-ttu-id="67455-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="67455-122">Resource Group Name</span></span>

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

### <span data-ttu-id="67455-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67455-123">CommonParameters</span></span>
<span data-ttu-id="67455-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67455-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67455-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67455-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67455-126">輸入</span><span class="sxs-lookup"><span data-stu-id="67455-126">INPUTS</span></span>

### <span data-ttu-id="67455-127">所有</span><span class="sxs-lookup"><span data-stu-id="67455-127">None</span></span>

## <span data-ttu-id="67455-128">輸出</span><span class="sxs-lookup"><span data-stu-id="67455-128">OUTPUTS</span></span>

### <span data-ttu-id="67455-129">WebApps WebApp. PSAppServicePlan （）</span><span class="sxs-lookup"><span data-stu-id="67455-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="67455-130">筆記</span><span class="sxs-lookup"><span data-stu-id="67455-130">NOTES</span></span>

## <span data-ttu-id="67455-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="67455-131">RELATED LINKS</span></span>

[<span data-ttu-id="67455-132">新-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67455-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="67455-133">移除-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67455-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="67455-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="67455-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


