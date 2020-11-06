---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 8bd043f11294b2290a5f54289232bc826c1f0d88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444043"
---
# <span data-ttu-id="dc620-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="dc620-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="dc620-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc620-102">SYNOPSIS</span></span>
<span data-ttu-id="dc620-103">重新生成自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="dc620-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc620-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc620-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc620-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc620-105">DESCRIPTION</span></span>
<span data-ttu-id="dc620-106">**新的-AzureRmAutomationKey** Cmdlet 會重新產生 Azure 自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="dc620-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="dc620-107">示例</span><span class="sxs-lookup"><span data-stu-id="dc620-107">EXAMPLES</span></span>

### <span data-ttu-id="dc620-108">範例1：為自動化帳戶重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="dc620-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="dc620-109">這個命令會在名為 ResourceGroup01 的資源群組中，重新生成名為 AutomationAccount01 的 Azure 自動化帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="dc620-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="dc620-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc620-110">PARAMETERS</span></span>

### <span data-ttu-id="dc620-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc620-111">-AutomationAccountName</span></span>
<span data-ttu-id="dc620-112">指定此 Cmdlet 重新生成金鑰的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="dc620-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="dc620-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc620-113">-DefaultProfile</span></span>
<span data-ttu-id="dc620-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc620-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc620-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="dc620-115">-KeyType</span></span>
<span data-ttu-id="dc620-116">指定代理程式註冊金鑰的類型。</span><span class="sxs-lookup"><span data-stu-id="dc620-116">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="dc620-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="dc620-117">Valid values are:</span></span> 
- <span data-ttu-id="dc620-118">首選</span><span class="sxs-lookup"><span data-stu-id="dc620-118">Primary</span></span> 
- <span data-ttu-id="dc620-119">備用</span><span class="sxs-lookup"><span data-stu-id="dc620-119">Secondary</span></span>

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

### <span data-ttu-id="dc620-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc620-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc620-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc620-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dc620-122">這個 Cmdlet 會在此參數指定的資源群組中，為自動化帳戶重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="dc620-122">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc620-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc620-123">CommonParameters</span></span>
<span data-ttu-id="dc620-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc620-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc620-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc620-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc620-126">輸入</span><span class="sxs-lookup"><span data-stu-id="dc620-126">INPUTS</span></span>

### <span data-ttu-id="dc620-127">System.object</span><span class="sxs-lookup"><span data-stu-id="dc620-127">System.String</span></span>

## <span data-ttu-id="dc620-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dc620-128">OUTPUTS</span></span>

### <span data-ttu-id="dc620-129">AgentRegistration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dc620-129">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="dc620-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dc620-130">NOTES</span></span>

## <span data-ttu-id="dc620-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc620-131">RELATED LINKS</span></span>
