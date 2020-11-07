---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationAccount.md
ms.openlocfilehash: 46d6ba805b6995c0d984149d699ce0679f682407
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958660"
---
# <span data-ttu-id="67199-101">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="67199-101">Get-AzAutomationAccount</span></span>

## <span data-ttu-id="67199-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67199-102">SYNOPSIS</span></span>
<span data-ttu-id="67199-103">取得資源群組中的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="67199-103">Gets Automation accounts in a resource group.</span></span>

## <span data-ttu-id="67199-104">句法</span><span class="sxs-lookup"><span data-stu-id="67199-104">SYNTAX</span></span>

### <span data-ttu-id="67199-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="67199-105">ByAll (Default)</span></span>
```
Get-AzAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67199-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67199-106">ByAutomationAccountName</span></span>
```
Get-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67199-107">說明</span><span class="sxs-lookup"><span data-stu-id="67199-107">DESCRIPTION</span></span>
<span data-ttu-id="67199-108">**AzAutomationAccount** Cmdlet 會取得資源群組中的 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="67199-108">The **Get-AzAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="67199-109">如需自動化帳戶的詳細資訊，請參閱 New-AzAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67199-109">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="67199-110">示例</span><span class="sxs-lookup"><span data-stu-id="67199-110">EXAMPLES</span></span>

### <span data-ttu-id="67199-111">範例1：取得所有帳戶</span><span class="sxs-lookup"><span data-stu-id="67199-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="67199-112">這個命令會取得名為 ResourceGroup03 的資源群組中的所有自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="67199-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="67199-113">範例2：取得帳戶</span><span class="sxs-lookup"><span data-stu-id="67199-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="67199-114">這個命令會在名為 ContosoResourceGroup 的資源群組中取得名為 ContosoAutomationAccount 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="67199-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="67199-115">參數</span><span class="sxs-lookup"><span data-stu-id="67199-115">PARAMETERS</span></span>

### <span data-ttu-id="67199-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67199-116">-DefaultProfile</span></span>
<span data-ttu-id="67199-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="67199-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67199-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="67199-118">-Name</span></span>
<span data-ttu-id="67199-119">指定此 Cmdlet 所取得之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="67199-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67199-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67199-120">-ResourceGroupName</span></span>
<span data-ttu-id="67199-121">指定此 Cmdlet 在其中取得自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67199-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="67199-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67199-122">CommonParameters</span></span>
<span data-ttu-id="67199-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67199-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67199-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67199-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67199-125">輸入</span><span class="sxs-lookup"><span data-stu-id="67199-125">INPUTS</span></span>

### <span data-ttu-id="67199-126">System.object</span><span class="sxs-lookup"><span data-stu-id="67199-126">System.String</span></span>

## <span data-ttu-id="67199-127">輸出</span><span class="sxs-lookup"><span data-stu-id="67199-127">OUTPUTS</span></span>

### <span data-ttu-id="67199-128">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="67199-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="67199-129">筆記</span><span class="sxs-lookup"><span data-stu-id="67199-129">NOTES</span></span>

## <span data-ttu-id="67199-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="67199-130">RELATED LINKS</span></span>

[<span data-ttu-id="67199-131">新-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="67199-131">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="67199-132">移除-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="67199-132">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="67199-133">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="67199-133">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


