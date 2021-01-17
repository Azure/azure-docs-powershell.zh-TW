---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447328"
---
# <span data-ttu-id="afe4f-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="afe4f-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="afe4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="afe4f-102">SYNOPSIS</span></span>
<span data-ttu-id="afe4f-103">從自動化取得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="afe4f-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="afe4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="afe4f-104">SYNTAX</span></span>

### <span data-ttu-id="afe4f-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="afe4f-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afe4f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="afe4f-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afe4f-107">說明</span><span class="sxs-lookup"><span data-stu-id="afe4f-107">DESCRIPTION</span></span>
<span data-ttu-id="afe4f-108">**AzAutomationModule** Cmdlet 會從 Azure 自動化取得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="afe4f-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="afe4f-109">示例</span><span class="sxs-lookup"><span data-stu-id="afe4f-109">EXAMPLES</span></span>

### <span data-ttu-id="afe4f-110">範例1：取得所有模組</span><span class="sxs-lookup"><span data-stu-id="afe4f-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="afe4f-111">這個命令會取得自動帳戶（名為 Contoso17）中的所有模組。</span><span class="sxs-lookup"><span data-stu-id="afe4f-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="afe4f-112">範例2：取得模組</span><span class="sxs-lookup"><span data-stu-id="afe4f-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="afe4f-113">這個命令會在自動化帳戶（名為 Contoso17）中取得名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="afe4f-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="afe4f-114">參數</span><span class="sxs-lookup"><span data-stu-id="afe4f-114">PARAMETERS</span></span>

### <span data-ttu-id="afe4f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="afe4f-115">-AutomationAccountName</span></span>
<span data-ttu-id="afe4f-116">指定此 Cmdlet 取得模組中繼資料之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="afe4f-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="afe4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe4f-117">-DefaultProfile</span></span>
<span data-ttu-id="afe4f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="afe4f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afe4f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="afe4f-119">-Name</span></span>
<span data-ttu-id="afe4f-120">指定此 Cmdlet 取得中繼資料的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="afe4f-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afe4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="afe4f-122">指定此 Cmdlet 取得模組中繼資料之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="afe4f-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="afe4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe4f-123">CommonParameters</span></span>
<span data-ttu-id="afe4f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="afe4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe4f-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="afe4f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe4f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="afe4f-126">INPUTS</span></span>

### <span data-ttu-id="afe4f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="afe4f-127">System.String</span></span>

## <span data-ttu-id="afe4f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="afe4f-128">OUTPUTS</span></span>

### <span data-ttu-id="afe4f-129">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="afe4f-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="afe4f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="afe4f-130">NOTES</span></span>

## <span data-ttu-id="afe4f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="afe4f-131">RELATED LINKS</span></span>

[<span data-ttu-id="afe4f-132">新-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="afe4f-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="afe4f-133">移除-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="afe4f-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="afe4f-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="afe4f-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


