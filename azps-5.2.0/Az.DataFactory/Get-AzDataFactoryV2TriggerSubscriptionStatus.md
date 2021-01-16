---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282335"
---
# <span data-ttu-id="1dc61-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1dc61-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1dc61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dc61-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc61-103">取得事件觸發程式的訂閱狀態，移至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="1dc61-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="1dc61-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dc61-104">SYNTAX</span></span>

### <span data-ttu-id="1dc61-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="1dc61-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc61-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1dc61-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dc61-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc61-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1dc61-108">說明</span><span class="sxs-lookup"><span data-stu-id="1dc61-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc61-109">這個命令會將事件觸發程式的訂閱狀態取得至指定的外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="1dc61-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="1dc61-110">在傳回的狀態為「已啟用」前，無法啟動觸發程式。</span><span class="sxs-lookup"><span data-stu-id="1dc61-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="1dc61-111">示例</span><span class="sxs-lookup"><span data-stu-id="1dc61-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc61-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1dc61-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="1dc61-113">這個命令會取得 subscribtion 的 BlobEnetTrigger1 觸發程式狀態至外部服務事件。</span><span class="sxs-lookup"><span data-stu-id="1dc61-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="1dc61-114">參數</span><span class="sxs-lookup"><span data-stu-id="1dc61-114">PARAMETERS</span></span>

### <span data-ttu-id="1dc61-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1dc61-115">-DataFactoryName</span></span>
<span data-ttu-id="1dc61-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc61-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc61-117">-DefaultProfile</span></span>
<span data-ttu-id="1dc61-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dc61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc61-119">-InputObject</span></span>
<span data-ttu-id="1dc61-120">觸發程式物件。</span><span class="sxs-lookup"><span data-stu-id="1dc61-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dc61-121">-Name</span></span>
<span data-ttu-id="1dc61-122">觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc61-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc61-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dc61-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dc61-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc61-125">-ResourceId</span></span>
<span data-ttu-id="1dc61-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dc61-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc61-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc61-127">CommonParameters</span></span>
<span data-ttu-id="1dc61-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dc61-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc61-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dc61-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc61-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1dc61-130">INPUTS</span></span>

### <span data-ttu-id="1dc61-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1dc61-131">System.String</span></span>
<span data-ttu-id="1dc61-132">PSTrigger 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="1dc61-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1dc61-133">輸出</span><span class="sxs-lookup"><span data-stu-id="1dc61-133">OUTPUTS</span></span>

### <span data-ttu-id="1dc61-134">PSTriggerSubscriptionStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="1dc61-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1dc61-135">筆記</span><span class="sxs-lookup"><span data-stu-id="1dc61-135">NOTES</span></span>

## <span data-ttu-id="1dc61-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dc61-136">RELATED LINKS</span></span>

