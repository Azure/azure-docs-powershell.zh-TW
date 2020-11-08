---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139946"
---
# <span data-ttu-id="4ca00-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="4ca00-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="4ca00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ca00-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca00-103">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="4ca00-103">List deleted workspaces.</span></span>

## <span data-ttu-id="4ca00-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ca00-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca00-105">說明</span><span class="sxs-lookup"><span data-stu-id="4ca00-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca00-106">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="4ca00-106">List deleted workspaces.</span></span>

## <span data-ttu-id="4ca00-107">示例</span><span class="sxs-lookup"><span data-stu-id="4ca00-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca00-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4ca00-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="4ca00-109">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="4ca00-109">List deleted workspaces.</span></span>

## <span data-ttu-id="4ca00-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ca00-110">PARAMETERS</span></span>

### <span data-ttu-id="4ca00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca00-111">-DefaultProfile</span></span>
<span data-ttu-id="4ca00-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ca00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca00-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca00-113">-ResourceGroupName</span></span>
<span data-ttu-id="4ca00-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ca00-114">The resource group name.</span></span>

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

### <span data-ttu-id="4ca00-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca00-115">CommonParameters</span></span>
<span data-ttu-id="4ca00-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ca00-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca00-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ca00-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca00-118">輸入</span><span class="sxs-lookup"><span data-stu-id="4ca00-118">INPUTS</span></span>

### <span data-ttu-id="4ca00-119">System.object</span><span class="sxs-lookup"><span data-stu-id="4ca00-119">System.String</span></span>

## <span data-ttu-id="4ca00-120">輸出</span><span class="sxs-lookup"><span data-stu-id="4ca00-120">OUTPUTS</span></span>

### <span data-ttu-id="4ca00-121">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="4ca00-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4ca00-122">筆記</span><span class="sxs-lookup"><span data-stu-id="4ca00-122">NOTES</span></span>

## <span data-ttu-id="4ca00-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ca00-123">RELATED LINKS</span></span>
