---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624330"
---
# <span data-ttu-id="27f33-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27f33-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="27f33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27f33-102">SYNOPSIS</span></span>
<span data-ttu-id="27f33-103">建立自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="27f33-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27f33-104">句法</span><span class="sxs-lookup"><span data-stu-id="27f33-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f33-105">說明</span><span class="sxs-lookup"><span data-stu-id="27f33-105">DESCRIPTION</span></span>
<span data-ttu-id="27f33-106">**新的-AzureRmAutomationAccount** Cmdlet 會在資源群組中建立 Azure 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="27f33-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="27f33-107">自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。</span><span class="sxs-lookup"><span data-stu-id="27f33-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="27f33-108">自動化資源包括 runbook、所需的狀態設定 (DSC) 設定、作業和資產。</span><span class="sxs-lookup"><span data-stu-id="27f33-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="27f33-109">示例</span><span class="sxs-lookup"><span data-stu-id="27f33-109">EXAMPLES</span></span>

### <span data-ttu-id="27f33-110">範例1：建立自動化帳戶</span><span class="sxs-lookup"><span data-stu-id="27f33-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="27f33-111">這個命令會在東美國地區建立名為 ContosoAutomationAccount 的新自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="27f33-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="27f33-112">參數</span><span class="sxs-lookup"><span data-stu-id="27f33-112">PARAMETERS</span></span>

### <span data-ttu-id="27f33-113">-位置</span><span class="sxs-lookup"><span data-stu-id="27f33-113">-Location</span></span>
<span data-ttu-id="27f33-114">指定此 Cmdlet 建立自動化帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="27f33-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="27f33-115">若要取得有效的位置，請使用 Get-AzureRMLocation Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27f33-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f33-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="27f33-116">-Name</span></span>
<span data-ttu-id="27f33-117">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="27f33-117">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f33-118">-方案</span><span class="sxs-lookup"><span data-stu-id="27f33-118">-Plan</span></span>
<span data-ttu-id="27f33-119">指定自動化帳戶的方案。</span><span class="sxs-lookup"><span data-stu-id="27f33-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="27f33-120">有效值為：</span><span class="sxs-lookup"><span data-stu-id="27f33-120">Valid values are:</span></span>

- <span data-ttu-id="27f33-121">空白</span><span class="sxs-lookup"><span data-stu-id="27f33-121">Basic</span></span>
- <span data-ttu-id="27f33-122">空閒</span><span class="sxs-lookup"><span data-stu-id="27f33-122">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27f33-123">-ResourceGroupName</span></span>
<span data-ttu-id="27f33-124">指定此 Cmdlet 新增自動化帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27f33-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="27f33-125">-標記</span><span class="sxs-lookup"><span data-stu-id="27f33-125">-Tags</span></span>
<span data-ttu-id="27f33-126">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="27f33-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="27f33-127">例如：</span><span class="sxs-lookup"><span data-stu-id="27f33-127">For example:</span></span>

<span data-ttu-id="27f33-128">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="27f33-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f33-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f33-129">-DefaultProfile</span></span>
<span data-ttu-id="27f33-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27f33-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27f33-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f33-131">CommonParameters</span></span>
<span data-ttu-id="27f33-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27f33-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f33-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27f33-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f33-134">輸入</span><span class="sxs-lookup"><span data-stu-id="27f33-134">INPUTS</span></span>

## <span data-ttu-id="27f33-135">輸出</span><span class="sxs-lookup"><span data-stu-id="27f33-135">OUTPUTS</span></span>

### <span data-ttu-id="27f33-136">AutomationAccount 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="27f33-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="27f33-137">筆記</span><span class="sxs-lookup"><span data-stu-id="27f33-137">NOTES</span></span>

## <span data-ttu-id="27f33-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="27f33-138">RELATED LINKS</span></span>

[<span data-ttu-id="27f33-139">AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27f33-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="27f33-140">移除-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27f33-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="27f33-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="27f33-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
