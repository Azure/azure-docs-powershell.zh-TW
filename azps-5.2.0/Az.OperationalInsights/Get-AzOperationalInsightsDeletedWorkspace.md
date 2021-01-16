---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278095"
---
# <span data-ttu-id="b65f6-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="b65f6-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="b65f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b65f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b65f6-103">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="b65f6-103">List deleted workspaces.</span></span>

## <span data-ttu-id="b65f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b65f6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="b65f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b65f6-106">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="b65f6-106">List deleted workspaces.</span></span>

## <span data-ttu-id="b65f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="b65f6-107">EXAMPLES</span></span>

### <span data-ttu-id="b65f6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b65f6-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="b65f6-109">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="b65f6-109">List deleted workspaces.</span></span>

## <span data-ttu-id="b65f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="b65f6-110">PARAMETERS</span></span>

### <span data-ttu-id="b65f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65f6-111">-DefaultProfile</span></span>
<span data-ttu-id="b65f6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b65f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="b65f6-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65f6-114">The resource group name.</span></span>

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

### <span data-ttu-id="b65f6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65f6-115">CommonParameters</span></span>
<span data-ttu-id="b65f6-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b65f6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65f6-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b65f6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65f6-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b65f6-118">INPUTS</span></span>

### <span data-ttu-id="b65f6-119">System.object</span><span class="sxs-lookup"><span data-stu-id="b65f6-119">System.String</span></span>

## <span data-ttu-id="b65f6-120">輸出</span><span class="sxs-lookup"><span data-stu-id="b65f6-120">OUTPUTS</span></span>

### <span data-ttu-id="b65f6-121">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="b65f6-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="b65f6-122">筆記</span><span class="sxs-lookup"><span data-stu-id="b65f6-122">NOTES</span></span>

## <span data-ttu-id="b65f6-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="b65f6-123">RELATED LINKS</span></span>
