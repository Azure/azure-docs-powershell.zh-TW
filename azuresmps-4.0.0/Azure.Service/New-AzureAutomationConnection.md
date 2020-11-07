---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967666"
---
# <span data-ttu-id="e0b89-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e0b89-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="e0b89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0b89-102">SYNOPSIS</span></span>

<span data-ttu-id="e0b89-103">在自動化建立連線。</span><span class="sxs-lookup"><span data-stu-id="e0b89-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="e0b89-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0b89-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0b89-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0b89-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e0b89-106">**新的-AzureAutomationConnection** Cmdlet 會在 Microsoft Azure 自動化中建立連線。</span><span class="sxs-lookup"><span data-stu-id="e0b89-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e0b89-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0b89-107">EXAMPLES</span></span>

## <span data-ttu-id="e0b89-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0b89-108">PARAMETERS</span></span>

### <span data-ttu-id="e0b89-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0b89-109">-AutomationAccountName</span></span>
<span data-ttu-id="e0b89-110">指定將儲存連接之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b89-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="e0b89-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="e0b89-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="e0b89-112">指定包含鍵/值對的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e0b89-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="e0b89-113">鍵代表指定連線類型上的連接欄位。</span><span class="sxs-lookup"><span data-stu-id="e0b89-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="e0b89-114">這些值代表要針對連接實例的每個連接欄位所儲存的特定值。</span><span class="sxs-lookup"><span data-stu-id="e0b89-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b89-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="e0b89-115">-ConnectionTypeName</span></span>
<span data-ttu-id="e0b89-116">指定連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b89-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="e0b89-117">-描述</span><span class="sxs-lookup"><span data-stu-id="e0b89-117">-Description</span></span>
<span data-ttu-id="e0b89-118">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="e0b89-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0b89-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0b89-119">-Name</span></span>
<span data-ttu-id="e0b89-120">指定連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b89-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="e0b89-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e0b89-121">-Profile</span></span>
<span data-ttu-id="e0b89-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e0b89-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0b89-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e0b89-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0b89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b89-124">CommonParameters</span></span>
<span data-ttu-id="e0b89-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0b89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b89-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0b89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b89-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e0b89-127">INPUTS</span></span>

## <span data-ttu-id="e0b89-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e0b89-128">OUTPUTS</span></span>

### <span data-ttu-id="e0b89-129">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="e0b89-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="e0b89-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e0b89-130">NOTES</span></span>

## <span data-ttu-id="e0b89-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0b89-131">RELATED LINKS</span></span>

[<span data-ttu-id="e0b89-132">AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e0b89-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="e0b89-133">移除-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="e0b89-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="e0b89-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="e0b89-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


