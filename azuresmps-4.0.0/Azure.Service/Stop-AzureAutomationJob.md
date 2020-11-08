---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967388"
---
# <span data-ttu-id="9ca05-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9ca05-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="9ca05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ca05-102">SYNOPSIS</span></span>

<span data-ttu-id="9ca05-103">停止自動化作業。</span><span class="sxs-lookup"><span data-stu-id="9ca05-103">Stops an Automation job.</span></span>

## <span data-ttu-id="9ca05-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ca05-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ca05-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ca05-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9ca05-106">**AzureAutomationJob** Cmdlet 會停止 Microsoft Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="9ca05-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="9ca05-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="9ca05-107">Specify a running automation job.</span></span>

## <span data-ttu-id="9ca05-108">示例</span><span class="sxs-lookup"><span data-stu-id="9ca05-108">EXAMPLES</span></span>

### <span data-ttu-id="9ca05-109">範例1：停止作業</span><span class="sxs-lookup"><span data-stu-id="9ca05-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="9ca05-110">這個命令會停止具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="9ca05-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="9ca05-111">參數</span><span class="sxs-lookup"><span data-stu-id="9ca05-111">PARAMETERS</span></span>

### <span data-ttu-id="9ca05-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ca05-112">-AutomationAccountName</span></span>
<span data-ttu-id="9ca05-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ca05-113">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca05-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="9ca05-114">-Id</span></span>
<span data-ttu-id="9ca05-115">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ca05-115">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca05-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9ca05-116">-Profile</span></span>
<span data-ttu-id="9ca05-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9ca05-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ca05-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9ca05-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ca05-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca05-119">CommonParameters</span></span>
<span data-ttu-id="9ca05-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ca05-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca05-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ca05-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca05-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9ca05-122">INPUTS</span></span>

## <span data-ttu-id="9ca05-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9ca05-123">OUTPUTS</span></span>

## <span data-ttu-id="9ca05-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9ca05-124">NOTES</span></span>

## <span data-ttu-id="9ca05-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ca05-125">RELATED LINKS</span></span>

[<span data-ttu-id="9ca05-126">AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9ca05-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="9ca05-127">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9ca05-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="9ca05-128">暫停-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="9ca05-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)

