---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationConnection.md
ms.openlocfilehash: 85d2e5d3044efe97eef2b4aa784d8767973682f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446567"
---
# <span data-ttu-id="75688-101">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="75688-101">Get-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="75688-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75688-102">SYNOPSIS</span></span>
<span data-ttu-id="75688-103">取得自動化連線。</span><span class="sxs-lookup"><span data-stu-id="75688-103">Gets an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75688-104">句法</span><span class="sxs-lookup"><span data-stu-id="75688-104">SYNTAX</span></span>

### <span data-ttu-id="75688-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="75688-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75688-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="75688-106">ByConnectionName</span></span>
```
Get-AzureRmAutomationConnection [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75688-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="75688-107">ByConnectionTypeName</span></span>
```
Get-AzureRmAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75688-108">說明</span><span class="sxs-lookup"><span data-stu-id="75688-108">DESCRIPTION</span></span>
<span data-ttu-id="75688-109">**AzureRmAutomationConnection** Cmdlet 會取得一或多個 Azure 自動化連線。</span><span class="sxs-lookup"><span data-stu-id="75688-109">The **Get-AzureRmAutomationConnection** cmdlet gets one or more Azure Automation connections.</span></span>
<span data-ttu-id="75688-110">根據預設，這個 Cmdlet 會檢索所有連線。</span><span class="sxs-lookup"><span data-stu-id="75688-110">By default, this cmdlet retrieves all connections.</span></span>
<span data-ttu-id="75688-111">指定連線的名稱以取得特定連線。</span><span class="sxs-lookup"><span data-stu-id="75688-111">Specify the name of a connection to get a specific connection.</span></span>
<span data-ttu-id="75688-112">指定連線類型名稱，以取得特定類型的所有連線。</span><span class="sxs-lookup"><span data-stu-id="75688-112">Specify the connection type name to get all connections of a specific type.</span></span>

## <span data-ttu-id="75688-113">示例</span><span class="sxs-lookup"><span data-stu-id="75688-113">EXAMPLES</span></span>

### <span data-ttu-id="75688-114">範例1：取得所有連線</span><span class="sxs-lookup"><span data-stu-id="75688-114">Example 1: Get all connections</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="75688-115">這個命令會針對自動化帳戶中名為 Contoso17 的所有連線取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="75688-115">This command gets metadata for all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="75688-116">範例2：取得某個類型的所有連接</span><span class="sxs-lookup"><span data-stu-id="75688-116">Example 2: Get all connections of a type</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

<span data-ttu-id="75688-117">這個命令會針對自動化帳戶（名為 Contoso17）中的連線取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="75688-117">This command gets metadata for connections in the Automation account named Contoso17.</span></span>
<span data-ttu-id="75688-118">這個命令會取得類型 SqlServer 的連線。</span><span class="sxs-lookup"><span data-stu-id="75688-118">This command gets connections of the type SqlServer.</span></span>

### <span data-ttu-id="75688-119">範例3：取得連線</span><span class="sxs-lookup"><span data-stu-id="75688-119">Example 3: Get a connection</span></span>
```
PS C:\>Get-AzureRmAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

<span data-ttu-id="75688-120">這個命令會取得名為 ContosoConnection 之連接的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="75688-120">This command gets metadata for the connection named ContosoConnection.</span></span>

## <span data-ttu-id="75688-121">參數</span><span class="sxs-lookup"><span data-stu-id="75688-121">PARAMETERS</span></span>

### <span data-ttu-id="75688-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="75688-122">-AutomationAccountName</span></span>
<span data-ttu-id="75688-123">指定此 Cmdlet 取得連接的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="75688-123">Specifies the name of the Automation account for which this cmdlet gets connections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75688-124">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="75688-124">-ConnectionTypeName</span></span>
<span data-ttu-id="75688-125">指定此 Cmdlet 為其檢索連線的連線類型名稱。</span><span class="sxs-lookup"><span data-stu-id="75688-125">Specifies the name of a connection type for which this cmdlet retrieves connections.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75688-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75688-126">-DefaultProfile</span></span>
<span data-ttu-id="75688-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="75688-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75688-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="75688-128">-Name</span></span>
<span data-ttu-id="75688-129">指定此 Cmdlet 所檢索的連線名稱。</span><span class="sxs-lookup"><span data-stu-id="75688-129">Specifies the name of a connection that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75688-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75688-130">-ResourceGroupName</span></span>
<span data-ttu-id="75688-131">指定此 Cmdlet 取得連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75688-131">Specifies the name of a resource group for which this cmdlet gets connections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75688-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75688-132">CommonParameters</span></span>
<span data-ttu-id="75688-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75688-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75688-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75688-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75688-135">輸入</span><span class="sxs-lookup"><span data-stu-id="75688-135">INPUTS</span></span>

### <span data-ttu-id="75688-136">所有</span><span class="sxs-lookup"><span data-stu-id="75688-136">None</span></span>
<span data-ttu-id="75688-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="75688-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75688-138">輸出</span><span class="sxs-lookup"><span data-stu-id="75688-138">OUTPUTS</span></span>

### <span data-ttu-id="75688-139">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="75688-139">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="75688-140">筆記</span><span class="sxs-lookup"><span data-stu-id="75688-140">NOTES</span></span>

## <span data-ttu-id="75688-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="75688-141">RELATED LINKS</span></span>

[<span data-ttu-id="75688-142">新-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="75688-142">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)

[<span data-ttu-id="75688-143">移除-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="75688-143">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


