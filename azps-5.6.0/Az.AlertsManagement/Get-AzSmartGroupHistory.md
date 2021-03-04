---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: 7a581d81938a647d845d2220b27347c1b42fcb03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904170"
---
# <span data-ttu-id="8e72e-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="8e72e-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="8e72e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e72e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e72e-103">獲得智慧型群組歷程記錄</span><span class="sxs-lookup"><span data-stu-id="8e72e-103">Gets smart group history</span></span>

## <span data-ttu-id="8e72e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e72e-104">SYNTAX</span></span>

### <span data-ttu-id="8e72e-105">BySmartGroupId (預設) </span><span class="sxs-lookup"><span data-stu-id="8e72e-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e72e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e72e-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e72e-107">描述</span><span class="sxs-lookup"><span data-stu-id="8e72e-107">DESCRIPTION</span></span>
<span data-ttu-id="8e72e-108">**Get-AzSmartGroupHistory** Cmdlet 會取得智慧型群組歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="8e72e-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="8e72e-109">例子</span><span class="sxs-lookup"><span data-stu-id="8e72e-109">EXAMPLES</span></span>

### <span data-ttu-id="8e72e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="8e72e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="8e72e-111">獲得智慧型群組歷程記錄詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8e72e-111">Gets smart group history details.</span></span>

## <span data-ttu-id="8e72e-112">參數</span><span class="sxs-lookup"><span data-stu-id="8e72e-112">PARAMETERS</span></span>

### <span data-ttu-id="8e72e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e72e-113">-DefaultProfile</span></span>
<span data-ttu-id="8e72e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e72e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e72e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e72e-115">-InputObject</span></span>
<span data-ttu-id="8e72e-116">來自管線的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8e72e-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="8e72e-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="8e72e-117">-SmartGroupId</span></span>
<span data-ttu-id="8e72e-118">通知的 SmartGroup/ResourceId 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e72e-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

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

### <span data-ttu-id="8e72e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e72e-119">CommonParameters</span></span>
<span data-ttu-id="8e72e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e72e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e72e-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e72e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e72e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8e72e-122">INPUTS</span></span>

### <span data-ttu-id="8e72e-123">沒有</span><span class="sxs-lookup"><span data-stu-id="8e72e-123">None</span></span>

## <span data-ttu-id="8e72e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8e72e-124">OUTPUTS</span></span>

### <span data-ttu-id="8e72e-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span><span class="sxs-lookup"><span data-stu-id="8e72e-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="8e72e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8e72e-126">NOTES</span></span>

## <span data-ttu-id="8e72e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e72e-127">RELATED LINKS</span></span>
