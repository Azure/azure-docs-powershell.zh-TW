---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B32A8423-A7AA-418E-A95D-6C18566741AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationAccount.md
ms.openlocfilehash: a72b7dcb729df3327277b2156574c5a0d5d9deb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444076"
---
# <span data-ttu-id="95641-101">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="95641-101">Get-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="95641-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95641-102">SYNOPSIS</span></span>
<span data-ttu-id="95641-103">取得資源群組中的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="95641-103">Gets Automation accounts in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95641-104">句法</span><span class="sxs-lookup"><span data-stu-id="95641-104">SYNTAX</span></span>

### <span data-ttu-id="95641-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="95641-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95641-106">ByAutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="95641-106">ByAutomationAccountName</span></span>
```
Get-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95641-107">說明</span><span class="sxs-lookup"><span data-stu-id="95641-107">DESCRIPTION</span></span>
<span data-ttu-id="95641-108">**AzureRmAutomationAccount** Cmdlet 會取得資源群組中的 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="95641-108">The **Get-AzureRmAutomationAccount** cmdlet gets Azure Automation accounts in a resource group.</span></span>
<span data-ttu-id="95641-109">如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95641-109">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="95641-110">示例</span><span class="sxs-lookup"><span data-stu-id="95641-110">EXAMPLES</span></span>

### <span data-ttu-id="95641-111">範例1：取得所有帳戶</span><span class="sxs-lookup"><span data-stu-id="95641-111">Example 1: Get all accounts</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="95641-112">這個命令會取得名為 ResourceGroup03 的資源群組中的所有自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="95641-112">This command gets all Automation accounts in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="95641-113">範例2：取得帳戶</span><span class="sxs-lookup"><span data-stu-id="95641-113">Example 2: Get an account</span></span>
```
PS C:\>Get-AzureRmAutomationAccount -ResourceGroupName "ResourceGroup03" -Name "ContosoAutomationAccount"
```

<span data-ttu-id="95641-114">這個命令會在名為 ContosoResourceGroup 的資源群組中取得名為 ContosoAutomationAccount 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="95641-114">This command gets the Automation account named ContosoAutomationAccount in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="95641-115">參數</span><span class="sxs-lookup"><span data-stu-id="95641-115">PARAMETERS</span></span>

### <span data-ttu-id="95641-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95641-116">-DefaultProfile</span></span>
<span data-ttu-id="95641-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95641-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95641-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="95641-118">-Name</span></span>
<span data-ttu-id="95641-119">指定此 Cmdlet 所取得之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="95641-119">Specifies the name of the Automation account that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95641-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95641-120">-ResourceGroupName</span></span>
<span data-ttu-id="95641-121">指定此 Cmdlet 在其中取得自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95641-121">Specifies the name of a resource group in which this cmdlet gets Automation accounts.</span></span>

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

### <span data-ttu-id="95641-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95641-122">CommonParameters</span></span>
<span data-ttu-id="95641-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95641-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95641-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95641-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95641-125">輸入</span><span class="sxs-lookup"><span data-stu-id="95641-125">INPUTS</span></span>

### <span data-ttu-id="95641-126">System.object</span><span class="sxs-lookup"><span data-stu-id="95641-126">System.String</span></span>

## <span data-ttu-id="95641-127">輸出</span><span class="sxs-lookup"><span data-stu-id="95641-127">OUTPUTS</span></span>

### <span data-ttu-id="95641-128">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="95641-128">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="95641-129">筆記</span><span class="sxs-lookup"><span data-stu-id="95641-129">NOTES</span></span>

## <span data-ttu-id="95641-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="95641-130">RELATED LINKS</span></span>

[<span data-ttu-id="95641-131">新-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="95641-131">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="95641-132">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="95641-132">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="95641-133">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="95641-133">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


