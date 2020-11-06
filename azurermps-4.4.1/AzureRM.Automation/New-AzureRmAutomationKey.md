---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 055526FA-5DB7-4F1D-81B3-5D9753283FE2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationKey.md
ms.openlocfilehash: 3b29d1b07ab0c11f42f1a7d4d9326ae19f6b79f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454931"
---
# <span data-ttu-id="0e6f4-101">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="0e6f4-101">New-AzureRmAutomationKey</span></span>

## <span data-ttu-id="0e6f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e6f4-103">重新生成自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-103">Regenerates registration keys for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e6f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e6f4-104">SYNTAX</span></span>

```
New-AzureRmAutomationKey [-KeyType] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e6f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e6f4-105">DESCRIPTION</span></span>
<span data-ttu-id="0e6f4-106">**新的-AzureRmAutomationKey** Cmdlet 會重新產生 Azure 自動化帳戶的註冊金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-106">The **New-AzureRmAutomationKey** cmdlet regenerates registration keys for an Azure Automation account.</span></span>

## <span data-ttu-id="0e6f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e6f4-107">EXAMPLES</span></span>

### <span data-ttu-id="0e6f4-108">範例1：為自動化帳戶重新產生金鑰</span><span class="sxs-lookup"><span data-stu-id="0e6f4-108">Example 1: Regenerate a key for an Automation account</span></span>
```
PS C:\>New-AzureAutomationKey -KeyType Primary -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0e6f4-109">這個命令會在名為 ResourceGroup01 的資源群組中，重新生成名為 AutomationAccount01 的 Azure 自動化帳戶的主鍵。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-109">This command regenerates the primary key for the Azure Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0e6f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e6f4-110">PARAMETERS</span></span>

### <span data-ttu-id="0e6f4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e6f4-111">-AutomationAccountName</span></span>
<span data-ttu-id="0e6f4-112">指定此 Cmdlet 重新生成金鑰的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-112">Specifies the name of an Automation account for which this cmdlet regenerates keys.</span></span>

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

### <span data-ttu-id="0e6f4-113">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0e6f4-113">-KeyType</span></span>
<span data-ttu-id="0e6f4-114">指定代理程式註冊金鑰的類型。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-114">Specifies the type of the agent registration key.</span></span>
<span data-ttu-id="0e6f4-115">有效值為：</span><span class="sxs-lookup"><span data-stu-id="0e6f4-115">Valid values are:</span></span> 

- <span data-ttu-id="0e6f4-116">首選</span><span class="sxs-lookup"><span data-stu-id="0e6f4-116">Primary</span></span> 
- <span data-ttu-id="0e6f4-117">備用</span><span class="sxs-lookup"><span data-stu-id="0e6f4-117">Secondary</span></span>

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

### <span data-ttu-id="0e6f4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e6f4-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e6f4-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0e6f4-120">這個 Cmdlet 會在此參數指定的資源群組中，為自動化帳戶重新產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-120">This cmdlet regenerates keys for an Automation account in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e6f4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e6f4-121">-DefaultProfile</span></span>
<span data-ttu-id="0e6f4-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e6f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e6f4-123">CommonParameters</span></span>
<span data-ttu-id="0e6f4-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e6f4-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e6f4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e6f4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0e6f4-126">INPUTS</span></span>

## <span data-ttu-id="0e6f4-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0e6f4-127">OUTPUTS</span></span>

### <span data-ttu-id="0e6f4-128">AgentRegistration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0e6f4-128">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="0e6f4-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0e6f4-129">NOTES</span></span>

## <span data-ttu-id="0e6f4-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e6f4-130">RELATED LINKS</span></span>

