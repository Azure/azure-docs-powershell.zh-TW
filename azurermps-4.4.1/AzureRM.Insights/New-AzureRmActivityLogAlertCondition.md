---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 058f828037ad546ea5ed66aaadeef579c4908930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626274"
---
# <span data-ttu-id="d67da-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="d67da-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="d67da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d67da-102">SYNOPSIS</span></span>
<span data-ttu-id="d67da-103">在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="d67da-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d67da-104">句法</span><span class="sxs-lookup"><span data-stu-id="d67da-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d67da-105">說明</span><span class="sxs-lookup"><span data-stu-id="d67da-105">DESCRIPTION</span></span>
<span data-ttu-id="d67da-106">**新的-AzureRmActivityLogAlertCondition** Cmdlet 會在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="d67da-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="d67da-107">示例</span><span class="sxs-lookup"><span data-stu-id="d67da-107">EXAMPLES</span></span>

### <span data-ttu-id="d67da-108">範例1：在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="d67da-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="d67da-109">這個命令會在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="d67da-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="d67da-110">**注意** ：與此 Cmdlet 搭配使用時 Set-AzureRmActivityLogAlert 至少其中一個傳送為參數的物件，其欄位必須等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="d67da-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="d67da-111">否則，後端會以 400 (BadRequest。 ) </span><span class="sxs-lookup"><span data-stu-id="d67da-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="d67da-112">參數</span><span class="sxs-lookup"><span data-stu-id="d67da-112">PARAMETERS</span></span>

### <span data-ttu-id="d67da-113">-欄位</span><span class="sxs-lookup"><span data-stu-id="d67da-113">-Field</span></span>
<span data-ttu-id="d67da-114">指定條件的欄位。</span><span class="sxs-lookup"><span data-stu-id="d67da-114">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67da-115">-等於</span><span class="sxs-lookup"><span data-stu-id="d67da-115">-Equal</span></span>
<span data-ttu-id="d67da-116">指定葉條件的 equals 屬性。</span><span class="sxs-lookup"><span data-stu-id="d67da-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d67da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67da-117">-DefaultProfile</span></span>
<span data-ttu-id="d67da-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d67da-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d67da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67da-119">CommonParameters</span></span>
<span data-ttu-id="d67da-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d67da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d67da-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d67da-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67da-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d67da-122">INPUTS</span></span>

## <span data-ttu-id="d67da-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d67da-123">OUTPUTS</span></span>

### <span data-ttu-id="d67da-124">ActivityLogAlertLeafCondition 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="d67da-124">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="d67da-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d67da-125">NOTES</span></span>

## <span data-ttu-id="d67da-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d67da-126">RELATED LINKS</span></span>

[<span data-ttu-id="d67da-127">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d67da-127">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d67da-128">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d67da-128">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d67da-129">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d67da-129">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d67da-130">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d67da-130">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d67da-131">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d67da-131">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d67da-132">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="d67da-132">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
