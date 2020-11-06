---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7ed232d14d215966b6cfad3ba788d3c80938316c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614131"
---
# <span data-ttu-id="c727b-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="c727b-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="c727b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c727b-102">SYNOPSIS</span></span>
<span data-ttu-id="c727b-103">取得智慧群組歷程記錄</span><span class="sxs-lookup"><span data-stu-id="c727b-103">Gets smart group history</span></span>

## <span data-ttu-id="c727b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c727b-104">SYNTAX</span></span>

### <span data-ttu-id="c727b-105">BySmartGroupId (預設) </span><span class="sxs-lookup"><span data-stu-id="c727b-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c727b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c727b-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c727b-107">說明</span><span class="sxs-lookup"><span data-stu-id="c727b-107">DESCRIPTION</span></span>
<span data-ttu-id="c727b-108">**AzSmartGroupHistory** Cmdlet 會取得智慧群組歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="c727b-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="c727b-109">示例</span><span class="sxs-lookup"><span data-stu-id="c727b-109">EXAMPLES</span></span>

### <span data-ttu-id="c727b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c727b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="c727b-111">取得智慧群組歷程記錄的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c727b-111">Gets smart group history details.</span></span>

## <span data-ttu-id="c727b-112">參數</span><span class="sxs-lookup"><span data-stu-id="c727b-112">PARAMETERS</span></span>

### <span data-ttu-id="c727b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c727b-113">-DefaultProfile</span></span>
<span data-ttu-id="c727b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c727b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c727b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c727b-115">-InputObject</span></span>
<span data-ttu-id="c727b-116">從管線輸入物件。</span><span class="sxs-lookup"><span data-stu-id="c727b-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c727b-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="c727b-117">-SmartGroupId</span></span>
<span data-ttu-id="c727b-118">警示的 SmartGroup/ResourceId 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c727b-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c727b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c727b-119">CommonParameters</span></span>
<span data-ttu-id="c727b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c727b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c727b-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c727b-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c727b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c727b-122">INPUTS</span></span>

### <span data-ttu-id="c727b-123">所有</span><span class="sxs-lookup"><span data-stu-id="c727b-123">None</span></span>

## <span data-ttu-id="c727b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c727b-124">OUTPUTS</span></span>

### <span data-ttu-id="c727b-125">AlertsManagement. OutputModels. PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="c727b-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="c727b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c727b-126">NOTES</span></span>

## <span data-ttu-id="c727b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c727b-127">RELATED LINKS</span></span>
