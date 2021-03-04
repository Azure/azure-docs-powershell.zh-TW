---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916310"
---
# <span data-ttu-id="a93dd-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a93dd-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="a93dd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a93dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a93dd-103">取得指定 Slot 名稱的路由規則。</span><span class="sxs-lookup"><span data-stu-id="a93dd-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="a93dd-104">語法</span><span class="sxs-lookup"><span data-stu-id="a93dd-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93dd-105">描述</span><span class="sxs-lookup"><span data-stu-id="a93dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a93dd-106">**Get-AzWebAppTrafficRouting** Cmdlet 從 Azure Web App Slot 取得路由規則組式。</span><span class="sxs-lookup"><span data-stu-id="a93dd-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="a93dd-107">例子</span><span class="sxs-lookup"><span data-stu-id="a93dd-107">EXAMPLES</span></span>

### <span data-ttu-id="a93dd-108">範例 1 從 Webapp 插槽中獲得特定的路由規則</span><span class="sxs-lookup"><span data-stu-id="a93dd-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="a93dd-109">此命令會針對一個網頁應用程式插槽獲得路由規則。</span><span class="sxs-lookup"><span data-stu-id="a93dd-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="a93dd-110">參數</span><span class="sxs-lookup"><span data-stu-id="a93dd-110">PARAMETERS</span></span>

### <span data-ttu-id="a93dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93dd-111">-DefaultProfile</span></span>
<span data-ttu-id="a93dd-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a93dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a93dd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93dd-113">-ResourceGroupName</span></span>
<span data-ttu-id="a93dd-114">資源組名</span><span class="sxs-lookup"><span data-stu-id="a93dd-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93dd-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="a93dd-115">-RuleName</span></span>
<span data-ttu-id="a93dd-116">規則名稱</span><span class="sxs-lookup"><span data-stu-id="a93dd-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93dd-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a93dd-117">-WebAppName</span></span>
<span data-ttu-id="a93dd-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a93dd-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93dd-119">CommonParameters</span></span>
<span data-ttu-id="a93dd-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a93dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93dd-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a93dd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93dd-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a93dd-122">INPUTS</span></span>

### <span data-ttu-id="a93dd-123">沒有</span><span class="sxs-lookup"><span data-stu-id="a93dd-123">None</span></span>

## <span data-ttu-id="a93dd-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a93dd-124">OUTPUTS</span></span>

### <span data-ttu-id="a93dd-125">Microsoft.Azure.management.Websites.models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="a93dd-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="a93dd-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a93dd-126">NOTES</span></span>

## <span data-ttu-id="a93dd-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a93dd-127">RELATED LINKS</span></span>

[<span data-ttu-id="a93dd-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a93dd-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a93dd-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a93dd-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="a93dd-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="a93dd-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
