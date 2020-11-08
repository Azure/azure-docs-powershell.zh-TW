---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970725"
---
# <span data-ttu-id="8ba4d-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="8ba4d-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="8ba4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ba4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba4d-103">取得警報歷程記錄資訊</span><span class="sxs-lookup"><span data-stu-id="8ba4d-103">Gets Alert History information</span></span>

## <span data-ttu-id="8ba4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ba4d-104">SYNTAX</span></span>

### <span data-ttu-id="8ba4d-105">ByAlertId (預設) </span><span class="sxs-lookup"><span data-stu-id="8ba4d-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ba4d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ba4d-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba4d-107">說明</span><span class="sxs-lookup"><span data-stu-id="8ba4d-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba4d-108">**AzAlertObjectHistory** Cmdlet 會取得警報的歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="8ba4d-109">示例</span><span class="sxs-lookup"><span data-stu-id="8ba4d-109">EXAMPLES</span></span>

### <span data-ttu-id="8ba4d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8ba4d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="8ba4d-111">取得警報歷程記錄的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-111">Gets alert history details.</span></span> 

## <span data-ttu-id="8ba4d-112">參數</span><span class="sxs-lookup"><span data-stu-id="8ba4d-112">PARAMETERS</span></span>

### <span data-ttu-id="8ba4d-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="8ba4d-113">-AlertId</span></span>
<span data-ttu-id="8ba4d-114">警示/警示的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="8ba4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba4d-115">-DefaultProfile</span></span>
<span data-ttu-id="8ba4d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba4d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba4d-117">-InputObject</span></span>
<span data-ttu-id="8ba4d-118">從管線輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="8ba4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba4d-119">CommonParameters</span></span>
<span data-ttu-id="8ba4d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba4d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8ba4d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba4d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8ba4d-122">INPUTS</span></span>

### <span data-ttu-id="8ba4d-123">所有</span><span class="sxs-lookup"><span data-stu-id="8ba4d-123">None</span></span>

## <span data-ttu-id="8ba4d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8ba4d-124">OUTPUTS</span></span>

### <span data-ttu-id="8ba4d-125">AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="8ba4d-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="8ba4d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8ba4d-126">NOTES</span></span>

## <span data-ttu-id="8ba4d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ba4d-127">RELATED LINKS</span></span>
