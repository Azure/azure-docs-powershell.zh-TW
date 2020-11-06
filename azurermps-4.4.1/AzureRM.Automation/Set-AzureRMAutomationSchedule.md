---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: 03763ad7c2212eb89650749eb6d407d9ce973693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447185"
---
# <span data-ttu-id="66dad-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="66dad-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="66dad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66dad-102">SYNOPSIS</span></span>
<span data-ttu-id="66dad-103">修改自動化排程。</span><span class="sxs-lookup"><span data-stu-id="66dad-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66dad-104">句法</span><span class="sxs-lookup"><span data-stu-id="66dad-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66dad-105">說明</span><span class="sxs-lookup"><span data-stu-id="66dad-105">DESCRIPTION</span></span>
<span data-ttu-id="66dad-106">**AzureRmAutomationSchedule** Cmdlet 會修改 Azure 自動化中的排程。</span><span class="sxs-lookup"><span data-stu-id="66dad-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="66dad-107">示例</span><span class="sxs-lookup"><span data-stu-id="66dad-107">EXAMPLES</span></span>

### <span data-ttu-id="66dad-108">範例1：修改排程</span><span class="sxs-lookup"><span data-stu-id="66dad-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="66dad-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="66dad-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="66dad-110">參數</span><span class="sxs-lookup"><span data-stu-id="66dad-110">PARAMETERS</span></span>

### <span data-ttu-id="66dad-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="66dad-111">-AutomationAccountName</span></span>
<span data-ttu-id="66dad-112">指定此 Cmdlet 修改排程的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="66dad-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="66dad-113">-描述</span><span class="sxs-lookup"><span data-stu-id="66dad-113">-Description</span></span>
<span data-ttu-id="66dad-114">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="66dad-114">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66dad-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="66dad-115">-IsEnabled</span></span>
<span data-ttu-id="66dad-116">指定此 Cmdlet 是否啟用排程。</span><span class="sxs-lookup"><span data-stu-id="66dad-116">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66dad-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="66dad-117">-Name</span></span>
<span data-ttu-id="66dad-118">指定此 Cmdlet 所修改之排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="66dad-118">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="66dad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dad-119">-ResourceGroupName</span></span>
<span data-ttu-id="66dad-120">指定此 Cmdlet 修改排程之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66dad-120">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="66dad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dad-121">-DefaultProfile</span></span>
<span data-ttu-id="66dad-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66dad-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66dad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dad-123">CommonParameters</span></span>
<span data-ttu-id="66dad-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66dad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dad-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66dad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dad-126">輸入</span><span class="sxs-lookup"><span data-stu-id="66dad-126">INPUTS</span></span>

## <span data-ttu-id="66dad-127">輸出</span><span class="sxs-lookup"><span data-stu-id="66dad-127">OUTPUTS</span></span>

### <span data-ttu-id="66dad-128">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="66dad-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="66dad-129">筆記</span><span class="sxs-lookup"><span data-stu-id="66dad-129">NOTES</span></span>

## <span data-ttu-id="66dad-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="66dad-130">RELATED LINKS</span></span>

[<span data-ttu-id="66dad-131">AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="66dad-131">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="66dad-132">新-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="66dad-132">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="66dad-133">移除-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="66dad-133">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)


