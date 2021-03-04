---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: a83028b47d487f4bbb2732497d7e9eefd01882ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907701"
---
# <span data-ttu-id="dc153-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="dc153-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="dc153-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc153-102">SYNOPSIS</span></span>
<span data-ttu-id="dc153-103">取得指定外部服務事件之事件觸發事件的訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="dc153-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="dc153-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc153-104">SYNTAX</span></span>

### <span data-ttu-id="dc153-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="dc153-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc153-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc153-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc153-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc153-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc153-108">描述</span><span class="sxs-lookup"><span data-stu-id="dc153-108">DESCRIPTION</span></span>
<span data-ttu-id="dc153-109">此命令會針對指定外部服務事件的事件觸發事件，獲得訂閱的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc153-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="dc153-110">在返回的狀態為「已啟用」之前，無法啟動觸發。</span><span class="sxs-lookup"><span data-stu-id="dc153-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="dc153-111">例子</span><span class="sxs-lookup"><span data-stu-id="dc153-111">EXAMPLES</span></span>

### <span data-ttu-id="dc153-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="dc153-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="dc153-113">此命令會取得 BlobEnetTri用1 觸發程式對外部服務事件的訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="dc153-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="dc153-114">參數</span><span class="sxs-lookup"><span data-stu-id="dc153-114">PARAMETERS</span></span>

### <span data-ttu-id="dc153-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dc153-115">-DataFactoryName</span></span>
<span data-ttu-id="dc153-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="dc153-116">The data factory name.</span></span>

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

### <span data-ttu-id="dc153-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc153-117">-DefaultProfile</span></span>
<span data-ttu-id="dc153-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc153-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc153-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc153-119">-InputObject</span></span>
<span data-ttu-id="dc153-120">觸發物件。</span><span class="sxs-lookup"><span data-stu-id="dc153-120">The trigger object.</span></span>

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

### <span data-ttu-id="dc153-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc153-121">-Name</span></span>
<span data-ttu-id="dc153-122">觸發者名稱。</span><span class="sxs-lookup"><span data-stu-id="dc153-122">The trigger name.</span></span>

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

### <span data-ttu-id="dc153-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc153-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc153-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="dc153-124">The resource group name.</span></span>

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

### <span data-ttu-id="dc153-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc153-125">-ResourceId</span></span>
<span data-ttu-id="dc153-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc153-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dc153-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc153-127">CommonParameters</span></span>
<span data-ttu-id="dc153-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc153-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc153-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dc153-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc153-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dc153-130">INPUTS</span></span>

### <span data-ttu-id="dc153-131">System.String</span><span class="sxs-lookup"><span data-stu-id="dc153-131">System.String</span></span>
<span data-ttu-id="dc153-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="dc153-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="dc153-133">輸出</span><span class="sxs-lookup"><span data-stu-id="dc153-133">OUTPUTS</span></span>

### <span data-ttu-id="dc153-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="dc153-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="dc153-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dc153-135">NOTES</span></span>

## <span data-ttu-id="dc153-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc153-136">RELATED LINKS</span></span>

