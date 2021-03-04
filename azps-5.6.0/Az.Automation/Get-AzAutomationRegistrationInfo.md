---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: aaa4a87f14572650fb0c1f969c11f0a3ed9cf0e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917497"
---
# <span data-ttu-id="1c23d-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="1c23d-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="1c23d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c23d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c23d-103">獲得將 DSC 節點或混合式員工上手至自動化的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="1c23d-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="1c23d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c23d-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c23d-105">描述</span><span class="sxs-lookup"><span data-stu-id="1c23d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c23d-106">**Get-AzAutomationRegistrationInfo** Cmdlet 會取得將想要的狀態組態 (DSC) 節點或混合式工作者上線至 Azure Automation 帳戶所需的端點和金鑰。</span><span class="sxs-lookup"><span data-stu-id="1c23d-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="1c23d-107">例子</span><span class="sxs-lookup"><span data-stu-id="1c23d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c23d-108">範例 1：取得註冊資訊</span><span class="sxs-lookup"><span data-stu-id="1c23d-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="1c23d-109">此命令會針對名為 ResourceGroup01 的資源群組中，名為 AutomationAccount01 的自動化帳戶，獲得註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="1c23d-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="1c23d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c23d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c23d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1c23d-111">-AutomationAccountName</span></span>
<span data-ttu-id="1c23d-112">指定此 Cmdlet 會獲得註冊資訊的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1c23d-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="1c23d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c23d-113">-DefaultProfile</span></span>
<span data-ttu-id="1c23d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1c23d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c23d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c23d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c23d-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c23d-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1c23d-117">此 Cmdlet 會針對此參數指定的資源群組，獲得註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="1c23d-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c23d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c23d-118">CommonParameters</span></span>
<span data-ttu-id="1c23d-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c23d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c23d-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1c23d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c23d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1c23d-121">INPUTS</span></span>

### <span data-ttu-id="1c23d-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1c23d-122">System.String</span></span>

## <span data-ttu-id="1c23d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1c23d-123">OUTPUTS</span></span>

### <span data-ttu-id="1c23d-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="1c23d-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="1c23d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1c23d-125">NOTES</span></span>

## <span data-ttu-id="1c23d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c23d-126">RELATED LINKS</span></span>

[<span data-ttu-id="1c23d-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1c23d-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="1c23d-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1c23d-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="1c23d-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="1c23d-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


