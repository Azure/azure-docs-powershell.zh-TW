---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450068"
---
# <span data-ttu-id="3240f-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="3240f-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="3240f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3240f-102">SYNOPSIS</span></span>
<span data-ttu-id="3240f-103">取得註冊資訊，以便將 DSC 節點或混合式輔助角色加入自動化。</span><span class="sxs-lookup"><span data-stu-id="3240f-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3240f-104">句法</span><span class="sxs-lookup"><span data-stu-id="3240f-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3240f-105">說明</span><span class="sxs-lookup"><span data-stu-id="3240f-105">DESCRIPTION</span></span>
<span data-ttu-id="3240f-106">**AzureRmAutomationRegistrationInfo** Cmdlet 會取得將 Desired) 節點或混合式輔助角色載入至 Azure 自動化帳戶的所需 (狀態設定所需的端點和按鍵。</span><span class="sxs-lookup"><span data-stu-id="3240f-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="3240f-107">示例</span><span class="sxs-lookup"><span data-stu-id="3240f-107">EXAMPLES</span></span>

### <span data-ttu-id="3240f-108">範例1：取得註冊資訊</span><span class="sxs-lookup"><span data-stu-id="3240f-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3240f-109">這個命令會取得名為 ResourceGroup01 之資源群組中名為 AutomationAccount01 之自動化帳戶的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="3240f-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="3240f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3240f-110">PARAMETERS</span></span>

### <span data-ttu-id="3240f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3240f-111">-AutomationAccountName</span></span>
<span data-ttu-id="3240f-112">指定此 Cmdlet 取得其註冊資訊的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3240f-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="3240f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3240f-113">-ResourceGroupName</span></span>
<span data-ttu-id="3240f-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3240f-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3240f-115">這個 Cmdlet 會取得此參數指定之資源群組的註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="3240f-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3240f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3240f-116">-DefaultProfile</span></span>
<span data-ttu-id="3240f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3240f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3240f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3240f-118">CommonParameters</span></span>
<span data-ttu-id="3240f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3240f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3240f-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3240f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3240f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="3240f-121">INPUTS</span></span>

## <span data-ttu-id="3240f-122">輸出</span><span class="sxs-lookup"><span data-stu-id="3240f-122">OUTPUTS</span></span>

### <span data-ttu-id="3240f-123">AgentRegistration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3240f-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="3240f-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3240f-124">NOTES</span></span>

## <span data-ttu-id="3240f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3240f-125">RELATED LINKS</span></span>

[<span data-ttu-id="3240f-126">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="3240f-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="3240f-127">AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3240f-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3240f-128">新-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="3240f-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


