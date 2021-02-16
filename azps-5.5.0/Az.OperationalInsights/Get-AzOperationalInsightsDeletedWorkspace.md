---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135619"
---
# <span data-ttu-id="23c72-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="23c72-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="23c72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23c72-102">SYNOPSIS</span></span>
<span data-ttu-id="23c72-103">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="23c72-103">List deleted workspaces.</span></span>

## <span data-ttu-id="23c72-104">句法</span><span class="sxs-lookup"><span data-stu-id="23c72-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c72-105">說明</span><span class="sxs-lookup"><span data-stu-id="23c72-105">DESCRIPTION</span></span>
<span data-ttu-id="23c72-106">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="23c72-106">List deleted workspaces.</span></span>

## <span data-ttu-id="23c72-107">示例</span><span class="sxs-lookup"><span data-stu-id="23c72-107">EXAMPLES</span></span>

### <span data-ttu-id="23c72-108">範例1</span><span class="sxs-lookup"><span data-stu-id="23c72-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="23c72-109">列出已刪除的工作區。</span><span class="sxs-lookup"><span data-stu-id="23c72-109">List deleted workspaces.</span></span>

## <span data-ttu-id="23c72-110">參數</span><span class="sxs-lookup"><span data-stu-id="23c72-110">PARAMETERS</span></span>

### <span data-ttu-id="23c72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c72-111">-DefaultProfile</span></span>
<span data-ttu-id="23c72-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23c72-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c72-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c72-113">-ResourceGroupName</span></span>
<span data-ttu-id="23c72-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23c72-114">The resource group name.</span></span>

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

### <span data-ttu-id="23c72-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c72-115">CommonParameters</span></span>
<span data-ttu-id="23c72-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23c72-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c72-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23c72-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c72-118">輸入</span><span class="sxs-lookup"><span data-stu-id="23c72-118">INPUTS</span></span>

### <span data-ttu-id="23c72-119">System.object</span><span class="sxs-lookup"><span data-stu-id="23c72-119">System.String</span></span>

## <span data-ttu-id="23c72-120">輸出</span><span class="sxs-lookup"><span data-stu-id="23c72-120">OUTPUTS</span></span>

### <span data-ttu-id="23c72-121">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="23c72-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="23c72-122">筆記</span><span class="sxs-lookup"><span data-stu-id="23c72-122">NOTES</span></span>

## <span data-ttu-id="23c72-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="23c72-123">RELATED LINKS</span></span>
