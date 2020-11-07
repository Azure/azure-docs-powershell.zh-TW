---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967817"
---
# <span data-ttu-id="aaa37-101">Get-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aaa37-101">Get-AzureAutomationAccount</span></span>

## <span data-ttu-id="aaa37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aaa37-102">SYNOPSIS</span></span>

<span data-ttu-id="aaa37-103">取得 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="aaa37-103">Gets Azure Automation accounts.</span></span>

## <span data-ttu-id="aaa37-104">句法</span><span class="sxs-lookup"><span data-stu-id="aaa37-104">SYNTAX</span></span>

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaa37-105">說明</span><span class="sxs-lookup"><span data-stu-id="aaa37-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="aaa37-106">**AzureAutomationAccount** Cmdlet 會為您的訂閱取得 Microsoft Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="aaa37-106">The **Get-AzureAutomationAccount** cmdlet gets the Microsoft Azure Automation accounts for your subscription.</span></span>
<span data-ttu-id="aaa37-107">自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。</span><span class="sxs-lookup"><span data-stu-id="aaa37-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span>
<span data-ttu-id="aaa37-108">自動化資源包括 runbook、工作和資產。</span><span class="sxs-lookup"><span data-stu-id="aaa37-108">Automation resources include runbooks, jobs, and assets.</span></span>

## <span data-ttu-id="aaa37-109">示例</span><span class="sxs-lookup"><span data-stu-id="aaa37-109">EXAMPLES</span></span>

### <span data-ttu-id="aaa37-110">範例1：取得自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="aaa37-110">Example 1: Get an Automation account</span></span>
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

<span data-ttu-id="aaa37-111">這個命令會取得名為 Contoso17 的自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="aaa37-111">This command gets the Automation account named Contoso17.</span></span>

## <span data-ttu-id="aaa37-112">參數</span><span class="sxs-lookup"><span data-stu-id="aaa37-112">PARAMETERS</span></span>

### <span data-ttu-id="aaa37-113">-位置</span><span class="sxs-lookup"><span data-stu-id="aaa37-113">-Location</span></span>
<span data-ttu-id="aaa37-114">指定與自動化帳戶相關聯的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="aaa37-114">Specifies an Azure location associated with Automation accounts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa37-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="aaa37-115">-Name</span></span>
<span data-ttu-id="aaa37-116">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="aaa37-116">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa37-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="aaa37-117">-Profile</span></span>
<span data-ttu-id="aaa37-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="aaa37-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aaa37-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="aaa37-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa37-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa37-120">CommonParameters</span></span>
<span data-ttu-id="aaa37-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aaa37-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa37-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aaa37-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa37-123">輸入</span><span class="sxs-lookup"><span data-stu-id="aaa37-123">INPUTS</span></span>

## <span data-ttu-id="aaa37-124">輸出</span><span class="sxs-lookup"><span data-stu-id="aaa37-124">OUTPUTS</span></span>

### <span data-ttu-id="aaa37-125">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="aaa37-125">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="aaa37-126">筆記</span><span class="sxs-lookup"><span data-stu-id="aaa37-126">NOTES</span></span>

## <span data-ttu-id="aaa37-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaa37-127">RELATED LINKS</span></span>

[<span data-ttu-id="aaa37-128">新-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aaa37-128">New-AzureAutomationAccount</span></span>](./New-AzureAutomationAccount.md)

[<span data-ttu-id="aaa37-129">移除-AzureAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="aaa37-129">Remove-AzureAutomationAccount</span></span>](./Remove-AzureAutomationAccount.md)


