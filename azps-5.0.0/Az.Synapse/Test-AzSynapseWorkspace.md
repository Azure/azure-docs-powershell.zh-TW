---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: b3dd32ec177aaa38e8fbb1f66559592f84905f2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136588"
---
# <span data-ttu-id="a4f71-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4f71-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="a4f71-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4f71-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f71-103">檢查是否存在 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="a4f71-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a4f71-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4f71-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4f71-105">說明</span><span class="sxs-lookup"><span data-stu-id="a4f71-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f71-106">**Test AzSynapseWorkspace** Cmdlet 會檢查是否存在 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="a4f71-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a4f71-107">示例</span><span class="sxs-lookup"><span data-stu-id="a4f71-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f71-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a4f71-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="a4f71-109">這個命令會檢查是否存在 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="a4f71-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="a4f71-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4f71-110">PARAMETERS</span></span>

### <span data-ttu-id="a4f71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f71-111">-DefaultProfile</span></span>
<span data-ttu-id="a4f71-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4f71-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4f71-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4f71-113">-Name</span></span>
<span data-ttu-id="a4f71-114">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f71-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f71-115">-ResourceGroupName</span></span>
<span data-ttu-id="a4f71-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a4f71-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f71-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f71-117">CommonParameters</span></span>
<span data-ttu-id="a4f71-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4f71-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f71-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4f71-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f71-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a4f71-120">INPUTS</span></span>

### <span data-ttu-id="a4f71-121">所有</span><span class="sxs-lookup"><span data-stu-id="a4f71-121">None</span></span>

## <span data-ttu-id="a4f71-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a4f71-122">OUTPUTS</span></span>

### <span data-ttu-id="a4f71-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a4f71-123">System.Object</span></span>
## <span data-ttu-id="a4f71-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a4f71-124">NOTES</span></span>

## <span data-ttu-id="a4f71-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4f71-125">RELATED LINKS</span></span>
