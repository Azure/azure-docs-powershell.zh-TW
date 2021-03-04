---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: 22b9d3322baa146bcd916024b15eea96b824f2eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915237"
---
# <span data-ttu-id="bb467-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="bb467-101">Get-AzLocation</span></span>

## <span data-ttu-id="bb467-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb467-102">SYNOPSIS</span></span>
<span data-ttu-id="bb467-103">獲得每個位置的所有位置和支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="bb467-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bb467-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb467-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb467-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb467-105">DESCRIPTION</span></span>
<span data-ttu-id="bb467-106">**Get-AzLocation** Cmdlet 會取得每個位置的所有位置和支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="bb467-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bb467-107">例子</span><span class="sxs-lookup"><span data-stu-id="bb467-107">EXAMPLES</span></span>

### <span data-ttu-id="bb467-108">範例 1：取得所有位置和支援的資源提供者</span><span class="sxs-lookup"><span data-stu-id="bb467-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="bb467-109">此命令會針對每個位置獲得所有位置和支援的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="bb467-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="bb467-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb467-110">PARAMETERS</span></span>

### <span data-ttu-id="bb467-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bb467-111">-ApiVersion</span></span>
<span data-ttu-id="bb467-112">指定資源提供者支援的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bb467-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="bb467-113">您可以指定與預設版本不同的版本。</span><span class="sxs-lookup"><span data-stu-id="bb467-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb467-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb467-114">-DefaultProfile</span></span>
<span data-ttu-id="bb467-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bb467-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb467-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="bb467-116">-Pre</span></span>
<span data-ttu-id="bb467-117">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bb467-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bb467-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb467-118">CommonParameters</span></span>
<span data-ttu-id="bb467-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb467-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb467-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb467-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb467-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bb467-121">INPUTS</span></span>

### <span data-ttu-id="bb467-122">沒有</span><span class="sxs-lookup"><span data-stu-id="bb467-122">None</span></span>

## <span data-ttu-id="bb467-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bb467-123">OUTPUTS</span></span>

### <span data-ttu-id="bb467-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="bb467-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="bb467-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bb467-125">NOTES</span></span>

## <span data-ttu-id="bb467-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb467-126">RELATED LINKS</span></span>
