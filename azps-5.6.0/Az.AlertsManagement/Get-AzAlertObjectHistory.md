---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 31b72f68151132fc4dca1bddd18c1a15b6a36f3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904177"
---
# <span data-ttu-id="a7d93-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="a7d93-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="a7d93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7d93-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d93-103">獲得提醒歷程記錄資訊</span><span class="sxs-lookup"><span data-stu-id="a7d93-103">Gets Alert History information</span></span>

## <span data-ttu-id="a7d93-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7d93-104">SYNTAX</span></span>

### <span data-ttu-id="a7d93-105">ByAlertId (預設) </span><span class="sxs-lookup"><span data-stu-id="a7d93-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d93-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a7d93-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7d93-107">描述</span><span class="sxs-lookup"><span data-stu-id="a7d93-107">DESCRIPTION</span></span>
<span data-ttu-id="a7d93-108">**Get-AzAlertObjectHistory Cmdlet** 會取得警示記錄。</span><span class="sxs-lookup"><span data-stu-id="a7d93-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="a7d93-109">例子</span><span class="sxs-lookup"><span data-stu-id="a7d93-109">EXAMPLES</span></span>

### <span data-ttu-id="a7d93-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a7d93-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="a7d93-111">獲得警示歷程記錄詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7d93-111">Gets alert history details.</span></span> 

## <span data-ttu-id="a7d93-112">參數</span><span class="sxs-lookup"><span data-stu-id="a7d93-112">PARAMETERS</span></span>

### <span data-ttu-id="a7d93-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="a7d93-113">-AlertId</span></span>
<span data-ttu-id="a7d93-114">警示的唯一識別碼/ ResourceId 警示。</span><span class="sxs-lookup"><span data-stu-id="a7d93-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7d93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d93-115">-DefaultProfile</span></span>
<span data-ttu-id="a7d93-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7d93-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d93-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7d93-117">-InputObject</span></span>
<span data-ttu-id="a7d93-118">來自管線的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a7d93-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="a7d93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d93-119">CommonParameters</span></span>
<span data-ttu-id="a7d93-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7d93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d93-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d93-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a7d93-122">INPUTS</span></span>

### <span data-ttu-id="a7d93-123">沒有</span><span class="sxs-lookup"><span data-stu-id="a7d93-123">None</span></span>

## <span data-ttu-id="a7d93-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a7d93-124">OUTPUTS</span></span>

### <span data-ttu-id="a7d93-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="a7d93-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="a7d93-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a7d93-126">NOTES</span></span>

## <span data-ttu-id="a7d93-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7d93-127">RELATED LINKS</span></span>
