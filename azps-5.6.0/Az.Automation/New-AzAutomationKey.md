---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 3116ee67b55df50d4dc79df2ee3faef3823878b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910557"
---
# <span data-ttu-id="f9eec-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="f9eec-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="f9eec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9eec-102">SYNOPSIS</span></span>
<span data-ttu-id="f9eec-103">重新產生自動化帳戶的登錄金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9eec-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="f9eec-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9eec-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9eec-105">描述</span><span class="sxs-lookup"><span data-stu-id="f9eec-105">DESCRIPTION</span></span>
<span data-ttu-id="f9eec-106">**New-AzAutomationKey** Cmdlet 會重新產生 Azure 自動化帳戶的登錄金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9eec-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="f9eec-107">例子</span><span class="sxs-lookup"><span data-stu-id="f9eec-107">EXAMPLES</span></span>

### <span data-ttu-id="f9eec-108">範例 1：重新產生自動化帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="f9eec-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="f9eec-109">此命令會重新產生名稱為 ResourceGroup01 的資源群組中名為 AutomationAccount01 的 Azure Automation 帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="f9eec-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f9eec-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9eec-110">PARAMETERS</span></span>

### <span data-ttu-id="f9eec-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f9eec-111">-AutomationAccountName</span></span>
<span data-ttu-id="f9eec-112">指定此 Cmdlet 會重新產生金鑰的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f9eec-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="f9eec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9eec-113">-DefaultProfile</span></span>
<span data-ttu-id="f9eec-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f9eec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9eec-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f9eec-115">-KeyType</span></span>
<span data-ttu-id="f9eec-116">指定代理程式註冊金鑰的類型。</span><span class="sxs-lookup"><span data-stu-id="f9eec-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="f9eec-117">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="f9eec-117">Valid values are:</span></span> 
- <span data-ttu-id="f9eec-118">主要</span><span class="sxs-lookup"><span data-stu-id="f9eec-118">Primary</span></span> 
- <span data-ttu-id="f9eec-119">二 次</span><span class="sxs-lookup"><span data-stu-id="f9eec-119">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9eec-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9eec-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9eec-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9eec-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f9eec-122">此 Cmdlet 會針對此參數指定的資源群組中的自動化帳戶重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="f9eec-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f9eec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9eec-123">CommonParameters</span></span>
<span data-ttu-id="f9eec-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9eec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9eec-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f9eec-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9eec-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f9eec-126">INPUTS</span></span>

### <span data-ttu-id="f9eec-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f9eec-127">System.String</span></span>

## <span data-ttu-id="f9eec-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f9eec-128">OUTPUTS</span></span>

### <span data-ttu-id="f9eec-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="f9eec-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="f9eec-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f9eec-130">NOTES</span></span>

## <span data-ttu-id="f9eec-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9eec-131">RELATED LINKS</span></span>
