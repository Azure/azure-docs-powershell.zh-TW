---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128631"
---
# <span data-ttu-id="0df17-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="0df17-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="0df17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0df17-102">SYNOPSIS</span></span>
<span data-ttu-id="0df17-103">傳回與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="0df17-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="0df17-104">句法</span><span class="sxs-lookup"><span data-stu-id="0df17-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df17-105">說明</span><span class="sxs-lookup"><span data-stu-id="0df17-105">DESCRIPTION</span></span>
<span data-ttu-id="0df17-106">**AzOperationalInsightsSchema** Cmdlet 會傳回與該資源群組中指定的工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="0df17-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="0df17-107">示例</span><span class="sxs-lookup"><span data-stu-id="0df17-107">EXAMPLES</span></span>

### <span data-ttu-id="0df17-108">範例1：取得工作區的架構</span><span class="sxs-lookup"><span data-stu-id="0df17-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="0df17-109">這個命令會取得與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="0df17-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="0df17-110">參數</span><span class="sxs-lookup"><span data-stu-id="0df17-110">PARAMETERS</span></span>

### <span data-ttu-id="0df17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df17-111">-DefaultProfile</span></span>
<span data-ttu-id="0df17-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0df17-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0df17-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df17-113">-ResourceGroupName</span></span>
<span data-ttu-id="0df17-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0df17-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df17-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0df17-115">-WorkspaceName</span></span>
<span data-ttu-id="0df17-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="0df17-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df17-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df17-117">CommonParameters</span></span>
<span data-ttu-id="0df17-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0df17-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df17-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0df17-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df17-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0df17-120">INPUTS</span></span>

### <span data-ttu-id="0df17-121">System.object</span><span class="sxs-lookup"><span data-stu-id="0df17-121">System.String</span></span>

## <span data-ttu-id="0df17-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0df17-122">OUTPUTS</span></span>

### <span data-ttu-id="0df17-123">PSSearchGetSchemaResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="0df17-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="0df17-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0df17-124">NOTES</span></span>

## <span data-ttu-id="0df17-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0df17-125">RELATED LINKS</span></span>

[<span data-ttu-id="0df17-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0df17-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


