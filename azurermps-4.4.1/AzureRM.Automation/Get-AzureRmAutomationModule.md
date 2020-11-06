---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450069"
---
# <span data-ttu-id="6f302-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f302-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="6f302-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f302-102">SYNOPSIS</span></span>
<span data-ttu-id="6f302-103">從自動化取得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6f302-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f302-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f302-104">SYNTAX</span></span>

### <span data-ttu-id="6f302-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="6f302-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f302-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f302-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f302-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f302-107">DESCRIPTION</span></span>
<span data-ttu-id="6f302-108">**AzureRmAutomationModule** Cmdlet 會從 Azure 自動化取得模組的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6f302-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="6f302-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f302-109">EXAMPLES</span></span>

### <span data-ttu-id="6f302-110">範例1：取得所有模組</span><span class="sxs-lookup"><span data-stu-id="6f302-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6f302-111">這個命令會取得自動帳戶（名為 Contoso17）中的所有模組。</span><span class="sxs-lookup"><span data-stu-id="6f302-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6f302-112">範例2：取得模組</span><span class="sxs-lookup"><span data-stu-id="6f302-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6f302-113">這個命令會在自動化帳戶（名為 Contoso17）中取得名為 ContosoModule 的模組。</span><span class="sxs-lookup"><span data-stu-id="6f302-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6f302-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f302-114">PARAMETERS</span></span>

### <span data-ttu-id="6f302-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f302-115">-AutomationAccountName</span></span>
<span data-ttu-id="6f302-116">指定此 Cmdlet 取得模組中繼資料之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f302-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="6f302-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f302-117">-Name</span></span>
<span data-ttu-id="6f302-118">指定此 Cmdlet 取得中繼資料的模組名稱。</span><span class="sxs-lookup"><span data-stu-id="6f302-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="6f302-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f302-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f302-120">指定此 Cmdlet 取得模組中繼資料之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f302-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="6f302-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f302-121">-DefaultProfile</span></span>
<span data-ttu-id="6f302-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f302-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f302-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f302-123">CommonParameters</span></span>
<span data-ttu-id="6f302-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f302-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f302-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f302-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f302-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6f302-126">INPUTS</span></span>

## <span data-ttu-id="6f302-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6f302-127">OUTPUTS</span></span>

### <span data-ttu-id="6f302-128">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="6f302-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="6f302-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6f302-129">NOTES</span></span>

## <span data-ttu-id="6f302-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f302-130">RELATED LINKS</span></span>

[<span data-ttu-id="6f302-131">新-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f302-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="6f302-132">移除-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f302-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="6f302-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6f302-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


