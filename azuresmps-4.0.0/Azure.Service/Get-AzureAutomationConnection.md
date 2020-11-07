---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967816"
---
# <span data-ttu-id="9189f-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9189f-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="9189f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9189f-102">SYNOPSIS</span></span>

<span data-ttu-id="9189f-103">取得 Azure 自動化連線。</span><span class="sxs-lookup"><span data-stu-id="9189f-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="9189f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9189f-104">SYNTAX</span></span>

### <span data-ttu-id="9189f-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="9189f-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9189f-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="9189f-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9189f-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9189f-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9189f-108">說明</span><span class="sxs-lookup"><span data-stu-id="9189f-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9189f-109">**AzureAutomationConnection** Cmdlet 會取得一或多個 Microsoft Azure 自動化連線。</span><span class="sxs-lookup"><span data-stu-id="9189f-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="9189f-110">根據預設，會傳回所有連接。</span><span class="sxs-lookup"><span data-stu-id="9189f-110">By default, all connections are returned.</span></span>
<span data-ttu-id="9189f-111">若要取得特定連接，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="9189f-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="9189f-112">若要取得特定類型的所有連接，請指定連線類型名稱。</span><span class="sxs-lookup"><span data-stu-id="9189f-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="9189f-113">示例</span><span class="sxs-lookup"><span data-stu-id="9189f-113">EXAMPLES</span></span>

### <span data-ttu-id="9189f-114">範例1：取得所有連線</span><span class="sxs-lookup"><span data-stu-id="9189f-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9189f-115">這個命令會取得自動帳戶（名為 Contoso17）中的所有連線。</span><span class="sxs-lookup"><span data-stu-id="9189f-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9189f-116">範例2：取得某個類型的所有連接</span><span class="sxs-lookup"><span data-stu-id="9189f-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="9189f-117">這個命令會取得名為 Contoso17 的自動化帳戶中的所有 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="9189f-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9189f-118">範例3：取得連線</span><span class="sxs-lookup"><span data-stu-id="9189f-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="9189f-119">這個命令會取得名為連線的連接。</span><span class="sxs-lookup"><span data-stu-id="9189f-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="9189f-120">參數</span><span class="sxs-lookup"><span data-stu-id="9189f-120">PARAMETERS</span></span>

### <span data-ttu-id="9189f-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9189f-121">-AutomationAccountName</span></span>
<span data-ttu-id="9189f-122">指定要取得連線的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9189f-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="9189f-123">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9189f-123">-ConnectionTypeName</span></span>
<span data-ttu-id="9189f-124">指定要檢索之連線之連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="9189f-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9189f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9189f-125">-Name</span></span>
<span data-ttu-id="9189f-126">指定要檢索的連線名稱。</span><span class="sxs-lookup"><span data-stu-id="9189f-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9189f-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9189f-127">-Profile</span></span>
<span data-ttu-id="9189f-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9189f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9189f-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9189f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9189f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9189f-130">CommonParameters</span></span>
<span data-ttu-id="9189f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9189f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9189f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9189f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9189f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9189f-133">INPUTS</span></span>

## <span data-ttu-id="9189f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9189f-134">OUTPUTS</span></span>

### <span data-ttu-id="9189f-135">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="9189f-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9189f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9189f-136">NOTES</span></span>

## <span data-ttu-id="9189f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9189f-137">RELATED LINKS</span></span>

[<span data-ttu-id="9189f-138">新-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9189f-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="9189f-139">移除-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9189f-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="9189f-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9189f-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


