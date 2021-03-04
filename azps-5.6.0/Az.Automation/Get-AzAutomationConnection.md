---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 5332cb1ca52a8ee3e7685ecf2fd36fd2333fd453
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913621"
---
# <span data-ttu-id="bcf16-101">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bcf16-101">Get-AzAutomationConnection</span></span>

## <span data-ttu-id="bcf16-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bcf16-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf16-103">進行自動化連接。</span><span class="sxs-lookup"><span data-stu-id="bcf16-103">Gets an Automation connection.</span></span>

## <span data-ttu-id="bcf16-104">語法</span><span class="sxs-lookup"><span data-stu-id="bcf16-104">SYNTAX</span></span>

### <span data-ttu-id="bcf16-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="bcf16-105">ByAll (Default)</span></span>
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf16-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="bcf16-106">ByConnectionName</span></span>
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf16-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="bcf16-107">ByConnectionTypeName</span></span>
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf16-108">描述</span><span class="sxs-lookup"><span data-stu-id="bcf16-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf16-109">**Get-AzAutomationConnection** Cmdlet 會取得一或多個 Azure 自動化連接。</span><span class="sxs-lookup"><span data-stu-id="bcf16-109">The **Get-AzAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="bcf16-110">根據預設，此 Cmdlet 會取回所有連結。</span><span class="sxs-lookup"><span data-stu-id="bcf16-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="bcf16-111">指定連接的名稱以取得特定連接。</span><span class="sxs-lookup"><span data-stu-id="bcf16-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="bcf16-112">指定連線類型名稱以取得特定類型的所有連接。</span><span class="sxs-lookup"><span data-stu-id="bcf16-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="bcf16-113">例子</span><span class="sxs-lookup"><span data-stu-id="bcf16-113">EXAMPLES</span></span>

### <span data-ttu-id="bcf16-114">範例 1：取得所有連結</span><span class="sxs-lookup"><span data-stu-id="bcf16-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bcf16-115">此命令會針對自動化帳戶名稱為 Contoso17 的所有連結，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bcf16-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bcf16-116">範例 2：取得類型的所有連結</span><span class="sxs-lookup"><span data-stu-id="bcf16-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="bcf16-117">此命令會針對名為 Contoso17 的自動化帳戶中的關聯，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bcf16-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="bcf16-118">此命令會獲得 SqlServer 類型的連結。</span><span class="sxs-lookup"><span data-stu-id="bcf16-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="bcf16-119">範例 3：取得連接</span><span class="sxs-lookup"><span data-stu-id="bcf16-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="bcf16-120">此命令會獲得名為 ContosoConnection 之連接的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bcf16-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="bcf16-121">參數</span><span class="sxs-lookup"><span data-stu-id="bcf16-121">PARAMETERS</span></span>

### <span data-ttu-id="bcf16-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bcf16-122">-AutomationAccountName</span></span>
<span data-ttu-id="bcf16-123">指定此 Cmdlet 可進行連結的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf16-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="bcf16-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="bcf16-124">-ConnectionTypeName</span></span>
<span data-ttu-id="bcf16-125">指定此 Cmdlet 會針對該 Cmdlet 所取取之連線類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf16-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf16-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf16-126">-DefaultProfile</span></span>
<span data-ttu-id="bcf16-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="bcf16-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcf16-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcf16-128">-Name</span></span>
<span data-ttu-id="bcf16-129">指定此 Cmdlet 所取取之連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcf16-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf16-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf16-130">-ResourceGroupName</span></span>
<span data-ttu-id="bcf16-131">指定此 Cmdlet 可進行連結的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bcf16-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

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

### <span data-ttu-id="bcf16-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf16-132">CommonParameters</span></span>
<span data-ttu-id="bcf16-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bcf16-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf16-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bcf16-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf16-135">輸入</span><span class="sxs-lookup"><span data-stu-id="bcf16-135">INPUTS</span></span>

### <span data-ttu-id="bcf16-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bcf16-136">System.String</span></span>

## <span data-ttu-id="bcf16-137">輸出</span><span class="sxs-lookup"><span data-stu-id="bcf16-137">OUTPUTS</span></span>

### <span data-ttu-id="bcf16-138">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="bcf16-138">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="bcf16-139">筆記</span><span class="sxs-lookup"><span data-stu-id="bcf16-139">NOTES</span></span>

## <span data-ttu-id="bcf16-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcf16-140">RELATED LINKS</span></span>

[<span data-ttu-id="bcf16-141">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bcf16-141">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)

[<span data-ttu-id="bcf16-142">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="bcf16-142">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


