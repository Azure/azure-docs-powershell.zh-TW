---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 0dcac3fac32094cf2d9a0e42abcffd6222783e78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450198"
---
# <span data-ttu-id="80471-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="80471-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="80471-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80471-102">SYNOPSIS</span></span>
<span data-ttu-id="80471-103">傳回與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="80471-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80471-104">句法</span><span class="sxs-lookup"><span data-stu-id="80471-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80471-105">說明</span><span class="sxs-lookup"><span data-stu-id="80471-105">DESCRIPTION</span></span>
<span data-ttu-id="80471-106">**AzureRmOperationalInsightsSchema** Cmdlet 會傳回與該資源群組中指定的工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="80471-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="80471-107">示例</span><span class="sxs-lookup"><span data-stu-id="80471-107">EXAMPLES</span></span>

### <span data-ttu-id="80471-108">範例1：取得工作區的架構</span><span class="sxs-lookup"><span data-stu-id="80471-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="80471-109">這個命令會取得與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="80471-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="80471-110">參數</span><span class="sxs-lookup"><span data-stu-id="80471-110">PARAMETERS</span></span>

### <span data-ttu-id="80471-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80471-111">-DefaultProfile</span></span>
<span data-ttu-id="80471-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="80471-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80471-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80471-113">-ResourceGroupName</span></span>
<span data-ttu-id="80471-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80471-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="80471-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80471-115">-WorkspaceName</span></span>
<span data-ttu-id="80471-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="80471-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="80471-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80471-117">CommonParameters</span></span>
<span data-ttu-id="80471-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80471-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80471-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80471-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80471-120">輸入</span><span class="sxs-lookup"><span data-stu-id="80471-120">INPUTS</span></span>

### <span data-ttu-id="80471-121">System.object</span><span class="sxs-lookup"><span data-stu-id="80471-121">System.String</span></span>

## <span data-ttu-id="80471-122">輸出</span><span class="sxs-lookup"><span data-stu-id="80471-122">OUTPUTS</span></span>

### <span data-ttu-id="80471-123">PSSearchGetSchemaResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="80471-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="80471-124">筆記</span><span class="sxs-lookup"><span data-stu-id="80471-124">NOTES</span></span>

## <span data-ttu-id="80471-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="80471-125">RELATED LINKS</span></span>

[<span data-ttu-id="80471-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80471-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


