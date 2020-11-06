---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 67100c80a3a0ca822fc1f37f63968be282925b76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445748"
---
# <span data-ttu-id="19121-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="19121-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="19121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19121-102">SYNOPSIS</span></span>
<span data-ttu-id="19121-103">停止自動化作業。</span><span class="sxs-lookup"><span data-stu-id="19121-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19121-104">句法</span><span class="sxs-lookup"><span data-stu-id="19121-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19121-105">說明</span><span class="sxs-lookup"><span data-stu-id="19121-105">DESCRIPTION</span></span>
<span data-ttu-id="19121-106">**AzureRmAutomationJob** Cmdlet 會停止 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="19121-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="19121-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="19121-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="19121-108">示例</span><span class="sxs-lookup"><span data-stu-id="19121-108">EXAMPLES</span></span>

### <span data-ttu-id="19121-109">範例1：停止作業</span><span class="sxs-lookup"><span data-stu-id="19121-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19121-110">這個命令會停止具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="19121-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="19121-111">參數</span><span class="sxs-lookup"><span data-stu-id="19121-111">PARAMETERS</span></span>

### <span data-ttu-id="19121-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19121-112">-AutomationAccountName</span></span>
<span data-ttu-id="19121-113">指定此 Cmdlet 停止作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="19121-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="19121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19121-114">-DefaultProfile</span></span>
<span data-ttu-id="19121-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="19121-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19121-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="19121-116">-Id</span></span>
<span data-ttu-id="19121-117">指定此 Cmdlet 停止的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="19121-117">Specifies the ID of a job that this cmdlet stops.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19121-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19121-118">-ResourceGroupName</span></span>
<span data-ttu-id="19121-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="19121-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="19121-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19121-120">CommonParameters</span></span>
<span data-ttu-id="19121-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19121-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19121-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="19121-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19121-123">輸入</span><span class="sxs-lookup"><span data-stu-id="19121-123">INPUTS</span></span>

### <span data-ttu-id="19121-124">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="19121-124">System.Guid</span></span>

### <span data-ttu-id="19121-125">System.object</span><span class="sxs-lookup"><span data-stu-id="19121-125">System.String</span></span>

## <span data-ttu-id="19121-126">輸出</span><span class="sxs-lookup"><span data-stu-id="19121-126">OUTPUTS</span></span>

### <span data-ttu-id="19121-127">System.void</span><span class="sxs-lookup"><span data-stu-id="19121-127">System.Void</span></span>

## <span data-ttu-id="19121-128">筆記</span><span class="sxs-lookup"><span data-stu-id="19121-128">NOTES</span></span>

## <span data-ttu-id="19121-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="19121-129">RELATED LINKS</span></span>

[<span data-ttu-id="19121-130">AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="19121-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="19121-131">AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="19121-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="19121-132">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="19121-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="19121-133">暫停-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="19121-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


