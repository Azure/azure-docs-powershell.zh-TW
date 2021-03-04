---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: df7266548b616615fa45131c21f40622894ffe9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904066"
---
# <span data-ttu-id="7d645-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="7d645-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="7d645-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7d645-102">SYNOPSIS</span></span>
<span data-ttu-id="7d645-103">此 Cmdlet 會針對每一份協定及控制項編號值，來取回特定的接收交換控制項編號。</span><span class="sxs-lookup"><span data-stu-id="7d645-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="7d645-104">語法</span><span class="sxs-lookup"><span data-stu-id="7d645-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d645-105">描述</span><span class="sxs-lookup"><span data-stu-id="7d645-105">DESCRIPTION</span></span>
<span data-ttu-id="7d645-106">此 Cmdlet 旨在用於災害復原案例，以驗證收到的交換控制項號碼是否存在，並且選擇性地使用 Remove-Az ScenarioAccountReceivedIcn 移除該實體。</span><span class="sxs-lookup"><span data-stu-id="7d645-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="7d645-107">請提供 "-AgreementType" 參數，以指定要傳回 X12 或 Edifact 控制項編號</span><span class="sxs-lookup"><span data-stu-id="7d645-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="7d645-108">例子</span><span class="sxs-lookup"><span data-stu-id="7d645-108">EXAMPLES</span></span>

### <span data-ttu-id="7d645-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="7d645-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="7d645-110">此命令會以協定名稱和控制項編號值，獲得 X12 整合帳戶收到的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="7d645-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="7d645-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="7d645-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="7d645-112">此命令會以協定名稱和控制項編號值，獲得 Edifact 整合帳戶收到的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="7d645-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="7d645-113">參數</span><span class="sxs-lookup"><span data-stu-id="7d645-113">PARAMETERS</span></span>

### <span data-ttu-id="7d645-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7d645-114">-AgreementName</span></span>
<span data-ttu-id="7d645-115">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="7d645-115">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d645-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7d645-116">-AgreementType</span></span>
<span data-ttu-id="7d645-117">整合帳戶協定類型。</span><span class="sxs-lookup"><span data-stu-id="7d645-117">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d645-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="7d645-118">-ControlNumberValue</span></span>
<span data-ttu-id="7d645-119">整合帳戶控制項數位值。</span><span class="sxs-lookup"><span data-stu-id="7d645-119">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d645-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d645-120">-DefaultProfile</span></span>
<span data-ttu-id="7d645-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7d645-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d645-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d645-122">-Name</span></span>
<span data-ttu-id="7d645-123">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7d645-123">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d645-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d645-124">-ResourceGroupName</span></span>
<span data-ttu-id="7d645-125">整合帳戶資源組名。</span><span class="sxs-lookup"><span data-stu-id="7d645-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="7d645-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d645-126">CommonParameters</span></span>
<span data-ttu-id="7d645-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7d645-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d645-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7d645-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d645-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7d645-129">INPUTS</span></span>

### <span data-ttu-id="7d645-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7d645-130">System.String</span></span>

## <span data-ttu-id="7d645-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7d645-131">OUTPUTS</span></span>

### <span data-ttu-id="7d645-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="7d645-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="7d645-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7d645-133">NOTES</span></span>

## <span data-ttu-id="7d645-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d645-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d645-135">Set-AzCountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="7d645-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="7d645-136">Remove-AzCountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="7d645-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
