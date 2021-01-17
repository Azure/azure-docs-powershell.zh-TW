---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CA25260C-D0BF-4F9C-A846-9D9B6C48CE8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationconnectionfieldvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationConnectionFieldValue.md
ms.openlocfilehash: 2df58153b2617a8ad62b0e46544128fa47a462b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447132"
---
# <span data-ttu-id="2f37d-101">Set-AzAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="2f37d-101">Set-AzAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="2f37d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f37d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f37d-103">修改自動化連線中欄位的值。</span><span class="sxs-lookup"><span data-stu-id="2f37d-103">Modifies the value of a field in an Automation connection.</span></span>

## <span data-ttu-id="2f37d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f37d-104">SYNTAX</span></span>

```
Set-AzAutomationConnectionFieldValue [-Name] <String> -ConnectionFieldName <String> -Value <Object>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f37d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f37d-105">DESCRIPTION</span></span>
<span data-ttu-id="2f37d-106">**AzAutomationConnectionFieldValue** Cmdlet 會修改 Azure 自動化中的連線中欄位的值。</span><span class="sxs-lookup"><span data-stu-id="2f37d-106">The **Set-AzAutomationConnectionFieldValue** cmdlet modifies the value of a field in a connection in Azure Automation.</span></span>

## <span data-ttu-id="2f37d-107">示例</span><span class="sxs-lookup"><span data-stu-id="2f37d-107">EXAMPLES</span></span>

### <span data-ttu-id="2f37d-108">範例1：變更連線中的欄位值</span><span class="sxs-lookup"><span data-stu-id="2f37d-108">Example 1: Change a field value in a connection</span></span>
```
PS C:\>Set-AzAutomationConnectionFieldValue -Name "ContosoConnection" -ConnectionFieldName "SubscriptionID" -Value "b53ec456-3494-4847-8f2b-180901c51050" -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="2f37d-109">這個命令會變更名為 AutomationAccount01 之自動化帳戶中名為 ContosoConnection 之 Azure 連線的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="2f37d-109">This command changes the subscription ID for the Azure connection named ContosoConnection in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="2f37d-110">參數</span><span class="sxs-lookup"><span data-stu-id="2f37d-110">PARAMETERS</span></span>

### <span data-ttu-id="2f37d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2f37d-111">-AutomationAccountName</span></span>
<span data-ttu-id="2f37d-112">指定此 Cmdlet 修改連線中之欄位之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f37d-112">Specifies the name of the Automation account for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2f37d-113">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="2f37d-113">-ConnectionFieldName</span></span>
<span data-ttu-id="2f37d-114">指定此 Cmdlet 所修改之欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f37d-114">Specifies a name for the field that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2f37d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f37d-115">-DefaultProfile</span></span>
<span data-ttu-id="2f37d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2f37d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f37d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f37d-117">-Name</span></span>
<span data-ttu-id="2f37d-118">指定此 Cmdlet 修改欄位之連接的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f37d-118">Specifies a name for the connection for which this cmdlet modifies a field.</span></span>

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

### <span data-ttu-id="2f37d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f37d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f37d-120">指定此 Cmdlet 在連線中修改欄位之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f37d-120">Specifies the name of the resource group for which this cmdlet modifies a field in a connection.</span></span>

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

### <span data-ttu-id="2f37d-121">-值</span><span class="sxs-lookup"><span data-stu-id="2f37d-121">-Value</span></span>
<span data-ttu-id="2f37d-122">在 [連接] 欄位中指定要修改的值。</span><span class="sxs-lookup"><span data-stu-id="2f37d-122">Specifies a value to modify in the connection field.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f37d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f37d-123">CommonParameters</span></span>
<span data-ttu-id="2f37d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f37d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f37d-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f37d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f37d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="2f37d-126">INPUTS</span></span>

### <span data-ttu-id="2f37d-127">System.object</span><span class="sxs-lookup"><span data-stu-id="2f37d-127">System.String</span></span>

### <span data-ttu-id="2f37d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2f37d-128">System.Object</span></span>

## <span data-ttu-id="2f37d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2f37d-129">OUTPUTS</span></span>

### <span data-ttu-id="2f37d-130">[-Azure. 命令. 自動化. 模型]。</span><span class="sxs-lookup"><span data-stu-id="2f37d-130">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="2f37d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2f37d-131">NOTES</span></span>

## <span data-ttu-id="2f37d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f37d-132">RELATED LINKS</span></span>

[<span data-ttu-id="2f37d-133">新-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="2f37d-133">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


