---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 52788c012a7da6013e58df924d1eda0a3aa5afcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786709"
---
# <span data-ttu-id="336d2-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="336d2-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="336d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="336d2-102">SYNOPSIS</span></span>
<span data-ttu-id="336d2-103">在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="336d2-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="336d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="336d2-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="336d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="336d2-105">DESCRIPTION</span></span>
<span data-ttu-id="336d2-106">**新的-AzActivityLogAlertCondition** Cmdlet 會在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="336d2-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="336d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="336d2-107">EXAMPLES</span></span>

### <span data-ttu-id="336d2-108">範例1：在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="336d2-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="336d2-109">這個命令會在記憶體中建立新的活動記錄警示條件物件。</span><span class="sxs-lookup"><span data-stu-id="336d2-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="336d2-110">**注意** ：與此 Cmdlet 搭配使用時 Set-AzActivityLogAlert 至少其中一個傳送為參數的物件，其欄位必須等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="336d2-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="336d2-111">否則，後端會以 400 (BadRequest。 ) </span><span class="sxs-lookup"><span data-stu-id="336d2-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="336d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="336d2-112">PARAMETERS</span></span>

### <span data-ttu-id="336d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336d2-113">-DefaultProfile</span></span>
<span data-ttu-id="336d2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="336d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="336d2-115">-等於</span><span class="sxs-lookup"><span data-stu-id="336d2-115">-Equal</span></span>
<span data-ttu-id="336d2-116">指定葉條件的 equals 屬性。</span><span class="sxs-lookup"><span data-stu-id="336d2-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="336d2-117">-欄位</span><span class="sxs-lookup"><span data-stu-id="336d2-117">-Field</span></span>
<span data-ttu-id="336d2-118">指定條件的欄位。</span><span class="sxs-lookup"><span data-stu-id="336d2-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="336d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336d2-119">CommonParameters</span></span>
<span data-ttu-id="336d2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="336d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336d2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="336d2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336d2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="336d2-122">INPUTS</span></span>

### <span data-ttu-id="336d2-123">System.object</span><span class="sxs-lookup"><span data-stu-id="336d2-123">System.String</span></span>

## <span data-ttu-id="336d2-124">輸出</span><span class="sxs-lookup"><span data-stu-id="336d2-124">OUTPUTS</span></span>

### <span data-ttu-id="336d2-125">ActivityLogAlertLeafCondition 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="336d2-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="336d2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="336d2-126">NOTES</span></span>

## <span data-ttu-id="336d2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="336d2-127">RELATED LINKS</span></span>

[<span data-ttu-id="336d2-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="336d2-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="336d2-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="336d2-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="336d2-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="336d2-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="336d2-131">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="336d2-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="336d2-132">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="336d2-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="336d2-133">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="336d2-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
