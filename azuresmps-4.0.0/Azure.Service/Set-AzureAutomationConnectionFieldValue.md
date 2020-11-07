---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967873"
---
# <span data-ttu-id="1ae19-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="1ae19-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="1ae19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ae19-102">SYNOPSIS</span></span>

<span data-ttu-id="1ae19-103">修改連線之欄位的值。</span><span class="sxs-lookup"><span data-stu-id="1ae19-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="1ae19-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ae19-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1ae19-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ae19-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1ae19-106">**AzureAutomationConnectionFieldValue** Cmdlet 會修改 Azure 自動化中連線之欄位的值。</span><span class="sxs-lookup"><span data-stu-id="1ae19-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="1ae19-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ae19-107">EXAMPLES</span></span>

## <span data-ttu-id="1ae19-108">參數</span><span class="sxs-lookup"><span data-stu-id="1ae19-108">PARAMETERS</span></span>

### <span data-ttu-id="1ae19-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ae19-109">-AutomationAccountName</span></span>
<span data-ttu-id="1ae19-110">指定連接的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae19-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae19-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="1ae19-111">-ConnectionFieldName</span></span>
<span data-ttu-id="1ae19-112">指定欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae19-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae19-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ae19-113">-Name</span></span>
<span data-ttu-id="1ae19-114">指定連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae19-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae19-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1ae19-115">-Profile</span></span>
<span data-ttu-id="1ae19-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1ae19-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1ae19-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1ae19-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ae19-118">-值</span><span class="sxs-lookup"><span data-stu-id="1ae19-118">-Value</span></span>
<span data-ttu-id="1ae19-119">指定要儲存在 [連接] 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="1ae19-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae19-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae19-120">CommonParameters</span></span>
<span data-ttu-id="1ae19-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ae19-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae19-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ae19-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae19-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1ae19-123">INPUTS</span></span>

## <span data-ttu-id="1ae19-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1ae19-124">OUTPUTS</span></span>

## <span data-ttu-id="1ae19-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1ae19-125">NOTES</span></span>

## <span data-ttu-id="1ae19-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ae19-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ae19-127">AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1ae19-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="1ae19-128">新-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1ae19-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="1ae19-129">移除-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1ae19-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


