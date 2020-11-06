---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationKey.md
ms.openlocfilehash: 1d0587ae9d1d45de4f08b71baa48ebb5e1633a36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613744"
---
# <span data-ttu-id="b6d68-101">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="b6d68-101">New-AzAutomationKey</span></span>

## <span data-ttu-id="b6d68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6d68-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d68-103">重新生成自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6d68-103">Regenerates registration keys for an Automation account.</span></span>

## <span data-ttu-id="b6d68-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6d68-104">SYNTAX</span></span>

```
New-AzAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6d68-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6d68-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d68-106">**新的-AzAutomationKey** Cmdlet 會重新產生 Azure 自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6d68-106">The **New-AzAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="b6d68-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6d68-107">EXAMPLES</span></span>

### <span data-ttu-id="b6d68-108">範例1：為自動化帳戶重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="b6d68-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="b6d68-109">這個命令會在名為 ResourceGroup01 的資源群組中，重新生成名為 AutomationAccount01 的 Azure 自動化帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="b6d68-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b6d68-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6d68-110">PARAMETERS</span></span>

### <span data-ttu-id="b6d68-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b6d68-111">-AutomationAccountName</span></span>
<span data-ttu-id="b6d68-112">指定此 Cmdlet 重新生成金鑰的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b6d68-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="b6d68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d68-113">-DefaultProfile</span></span>
<span data-ttu-id="b6d68-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b6d68-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6d68-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="b6d68-115">-KeyType</span></span>
<span data-ttu-id="b6d68-116">指定代理程式註冊金鑰的類型。</span><span class="sxs-lookup"><span data-stu-id="b6d68-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="b6d68-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="b6d68-117">Valid values are:</span></span> 
- <span data-ttu-id="b6d68-118">首選</span><span class="sxs-lookup"><span data-stu-id="b6d68-118">Primary</span></span> 
- <span data-ttu-id="b6d68-119">備用</span><span class="sxs-lookup"><span data-stu-id="b6d68-119">Secondary</span></span>

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

### <span data-ttu-id="b6d68-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d68-120">-ResourceGroupName</span></span>
<span data-ttu-id="b6d68-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6d68-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b6d68-122">這個 Cmdlet 會在此參數指定的資源群組中，為自動化帳戶重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6d68-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6d68-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d68-123">CommonParameters</span></span>
<span data-ttu-id="b6d68-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6d68-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d68-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6d68-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d68-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b6d68-126">INPUTS</span></span>

### <span data-ttu-id="b6d68-127">System.object</span><span class="sxs-lookup"><span data-stu-id="b6d68-127">System.String</span></span>

## <span data-ttu-id="b6d68-128">輸出</span><span class="sxs-lookup"><span data-stu-id="b6d68-128">OUTPUTS</span></span>

### <span data-ttu-id="b6d68-129">AgentRegistration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b6d68-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="b6d68-130">筆記</span><span class="sxs-lookup"><span data-stu-id="b6d68-130">NOTES</span></span>

## <span data-ttu-id="b6d68-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6d68-131">RELATED LINKS</span></span>