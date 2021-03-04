---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: a4ac55c3c00ba35fa53f6e9a338712d02e507ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908050"
---
# <span data-ttu-id="41840-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="41840-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="41840-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41840-102">SYNOPSIS</span></span>
<span data-ttu-id="41840-103">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="41840-103">List deleted workspaces.</span></span>

## <span data-ttu-id="41840-104">語法</span><span class="sxs-lookup"><span data-stu-id="41840-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41840-105">描述</span><span class="sxs-lookup"><span data-stu-id="41840-105">DESCRIPTION</span></span>
<span data-ttu-id="41840-106">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="41840-106">List deleted workspaces.</span></span>

## <span data-ttu-id="41840-107">例子</span><span class="sxs-lookup"><span data-stu-id="41840-107">EXAMPLES</span></span>

### <span data-ttu-id="41840-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="41840-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="41840-109">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="41840-109">List deleted workspaces.</span></span>

## <span data-ttu-id="41840-110">參數</span><span class="sxs-lookup"><span data-stu-id="41840-110">PARAMETERS</span></span>

### <span data-ttu-id="41840-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41840-111">-DefaultProfile</span></span>
<span data-ttu-id="41840-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="41840-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41840-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41840-113">-ResourceGroupName</span></span>
<span data-ttu-id="41840-114">資源組名。</span><span class="sxs-lookup"><span data-stu-id="41840-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41840-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41840-115">CommonParameters</span></span>
<span data-ttu-id="41840-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41840-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41840-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41840-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41840-118">輸入</span><span class="sxs-lookup"><span data-stu-id="41840-118">INPUTS</span></span>

### <span data-ttu-id="41840-119">System.String</span><span class="sxs-lookup"><span data-stu-id="41840-119">System.String</span></span>

## <span data-ttu-id="41840-120">輸出</span><span class="sxs-lookup"><span data-stu-id="41840-120">OUTPUTS</span></span>

### <span data-ttu-id="41840-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="41840-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="41840-122">筆記</span><span class="sxs-lookup"><span data-stu-id="41840-122">NOTES</span></span>

## <span data-ttu-id="41840-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="41840-123">RELATED LINKS</span></span>
