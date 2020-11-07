---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 635b08c90ea87dab98b724110b2228f5b46d61fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623486"
---
# <span data-ttu-id="336d9-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="336d9-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="336d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="336d9-102">SYNOPSIS</span></span>
<span data-ttu-id="336d9-103">繼續已暫停的自動作業。</span><span class="sxs-lookup"><span data-stu-id="336d9-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="336d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="336d9-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="336d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="336d9-105">DESCRIPTION</span></span>
<span data-ttu-id="336d9-106">**Resume AzureRmAutomationJob** Cmdlet 會繼續執行暫停的 Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="336d9-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="336d9-107">指定暫停的作業。</span><span class="sxs-lookup"><span data-stu-id="336d9-107">Specify the suspended job.</span></span>

<span data-ttu-id="336d9-108">若要暫停作業，請使用 Suspend-AzureRmAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="336d9-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="336d9-109">示例</span><span class="sxs-lookup"><span data-stu-id="336d9-109">EXAMPLES</span></span>

### <span data-ttu-id="336d9-110">範例1：繼續暫停的作業</span><span class="sxs-lookup"><span data-stu-id="336d9-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="336d9-111">這個命令會繼續執行具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="336d9-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="336d9-112">參數</span><span class="sxs-lookup"><span data-stu-id="336d9-112">PARAMETERS</span></span>

### <span data-ttu-id="336d9-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="336d9-113">-AutomationAccountName</span></span>
<span data-ttu-id="336d9-114">指定此 Cmdlet 繼續作業的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="336d9-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="336d9-115">-DefaultProfile</span></span>
<span data-ttu-id="336d9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="336d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336d9-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="336d9-117">-Id</span></span>
<span data-ttu-id="336d9-118">指定此 Cmdlet 繼續的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="336d9-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="336d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="336d9-120">指定此 Cmdlet 繼續作業之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="336d9-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336d9-121">CommonParameters</span></span>
<span data-ttu-id="336d9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="336d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336d9-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="336d9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336d9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="336d9-124">INPUTS</span></span>

### <span data-ttu-id="336d9-125">所有</span><span class="sxs-lookup"><span data-stu-id="336d9-125">None</span></span>
<span data-ttu-id="336d9-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="336d9-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="336d9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="336d9-127">OUTPUTS</span></span>

## <span data-ttu-id="336d9-128">筆記</span><span class="sxs-lookup"><span data-stu-id="336d9-128">NOTES</span></span>

## <span data-ttu-id="336d9-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="336d9-129">RELATED LINKS</span></span>

[<span data-ttu-id="336d9-130">AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="336d9-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="336d9-131">AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="336d9-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="336d9-132">停止 AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="336d9-132">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="336d9-133">暫停-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="336d9-133">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


