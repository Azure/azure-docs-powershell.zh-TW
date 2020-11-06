---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623019"
---
# <span data-ttu-id="83a63-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="83a63-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="83a63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83a63-102">SYNOPSIS</span></span>
<span data-ttu-id="83a63-103">建立自動化連線。</span><span class="sxs-lookup"><span data-stu-id="83a63-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="83a63-104">句法</span><span class="sxs-lookup"><span data-stu-id="83a63-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83a63-105">說明</span><span class="sxs-lookup"><span data-stu-id="83a63-105">DESCRIPTION</span></span>
<span data-ttu-id="83a63-106">**新的-AzAutomationConnection** Cmdlet 會在 Azure 自動化中建立連線。</span><span class="sxs-lookup"><span data-stu-id="83a63-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="83a63-107">示例</span><span class="sxs-lookup"><span data-stu-id="83a63-107">EXAMPLES</span></span>

### <span data-ttu-id="83a63-108">範例1：建立連線</span><span class="sxs-lookup"><span data-stu-id="83a63-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="83a63-109">第一個命令會將欄位值的雜湊表指派給 $FieldValue 變數。</span><span class="sxs-lookup"><span data-stu-id="83a63-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="83a63-110">第二個命令會在名為 AutomationAccount01 的自動化帳戶中，建立名為 Connection12 的 Azure 連線。</span><span class="sxs-lookup"><span data-stu-id="83a63-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="83a63-111">命令在 $FieldValues 中使用連接欄位的值。</span><span class="sxs-lookup"><span data-stu-id="83a63-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="83a63-112">參數</span><span class="sxs-lookup"><span data-stu-id="83a63-112">PARAMETERS</span></span>

### <span data-ttu-id="83a63-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="83a63-113">-AutomationAccountName</span></span>
<span data-ttu-id="83a63-114">指定此 Cmdlet 建立連線之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a63-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a63-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="83a63-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="83a63-116">指定包含鍵/值對的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="83a63-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="83a63-117">鍵代表指定連線類型的連接欄位。</span><span class="sxs-lookup"><span data-stu-id="83a63-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="83a63-118">這些值代表連接實例之每個連接欄位的特定值。</span><span class="sxs-lookup"><span data-stu-id="83a63-118">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a63-119">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="83a63-119">-ConnectionTypeName</span></span>
<span data-ttu-id="83a63-120">指定連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a63-120">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83a63-121">-DefaultProfile</span></span>
<span data-ttu-id="83a63-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="83a63-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83a63-123">-描述</span><span class="sxs-lookup"><span data-stu-id="83a63-123">-Description</span></span>
<span data-ttu-id="83a63-124">指定連線的描述。</span><span class="sxs-lookup"><span data-stu-id="83a63-124">Specifies a description for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a63-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="83a63-125">-Name</span></span>
<span data-ttu-id="83a63-126">指定連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a63-126">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83a63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83a63-127">-ResourceGroupName</span></span>
<span data-ttu-id="83a63-128">指定此 Cmdlet 建立連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83a63-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="83a63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83a63-129">CommonParameters</span></span>
<span data-ttu-id="83a63-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83a63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83a63-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83a63-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83a63-132">輸入</span><span class="sxs-lookup"><span data-stu-id="83a63-132">INPUTS</span></span>

### <span data-ttu-id="83a63-133">System.object</span><span class="sxs-lookup"><span data-stu-id="83a63-133">System.String</span></span>

### <span data-ttu-id="83a63-134">System.object</span><span class="sxs-lookup"><span data-stu-id="83a63-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="83a63-135">輸出</span><span class="sxs-lookup"><span data-stu-id="83a63-135">OUTPUTS</span></span>

### <span data-ttu-id="83a63-136">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="83a63-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="83a63-137">筆記</span><span class="sxs-lookup"><span data-stu-id="83a63-137">NOTES</span></span>

## <span data-ttu-id="83a63-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="83a63-138">RELATED LINKS</span></span>

[<span data-ttu-id="83a63-139">AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="83a63-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="83a63-140">移除-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="83a63-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


