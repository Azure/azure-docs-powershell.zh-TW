---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: f88ff018f38040573783aff58287b4788017566a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913622"
---
# <span data-ttu-id="fb317-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fb317-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="fb317-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fb317-102">SYNOPSIS</span></span>
<span data-ttu-id="fb317-103">在資源群組中獲取自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb317-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="fb317-104">語法</span><span class="sxs-lookup"><span data-stu-id="fb317-104">SYNTAX</span></span>

### <span data-ttu-id="fb317-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="fb317-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb317-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb317-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb317-107">描述</span><span class="sxs-lookup"><span data-stu-id="fb317-107">DESCRIPTION</span></span>
<span data-ttu-id="fb317-108">**Get-AzAutomationAccount** Cmdlet 會取得資源群組中的 Azure Automation 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb317-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="fb317-109">有關自動化帳戶的資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb317-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="fb317-110">例子</span><span class="sxs-lookup"><span data-stu-id="fb317-110">EXAMPLES</span></span>

### <span data-ttu-id="fb317-111">範例 1：取得所有帳戶</span><span class="sxs-lookup"><span data-stu-id="fb317-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="fb317-112">此命令會獲得資源群組中名為 ResourceGroup03 的所有自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb317-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="fb317-113">範例 2：取得帳戶</span><span class="sxs-lookup"><span data-stu-id="fb317-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="fb317-114">此命令在名為 ContosoResourceGroup 的資源群組中，會獲得名為 ContosoAutomationAccount 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb317-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="fb317-115">參數</span><span class="sxs-lookup"><span data-stu-id="fb317-115">PARAMETERS</span></span>

### <span data-ttu-id="fb317-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb317-116">-DefaultProfile</span></span>
<span data-ttu-id="fb317-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fb317-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb317-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb317-118">-Name</span></span>
<span data-ttu-id="fb317-119">指定此 Cmdlet 所獲取的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fb317-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb317-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb317-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb317-121">指定此 Cmdlet 會獲得自動化帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fb317-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByAutomationAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb317-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb317-122">CommonParameters</span></span>
<span data-ttu-id="fb317-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fb317-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb317-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fb317-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb317-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fb317-125">INPUTS</span></span>

### <span data-ttu-id="fb317-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fb317-126">System.String</span></span>

## <span data-ttu-id="fb317-127">輸出</span><span class="sxs-lookup"><span data-stu-id="fb317-127">OUTPUTS</span></span>

### <span data-ttu-id="fb317-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fb317-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="fb317-129">筆記</span><span class="sxs-lookup"><span data-stu-id="fb317-129">NOTES</span></span>

## <span data-ttu-id="fb317-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb317-130">RELATED LINKS</span></span>

[<span data-ttu-id="fb317-131">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fb317-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="fb317-132">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fb317-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="fb317-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fb317-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


