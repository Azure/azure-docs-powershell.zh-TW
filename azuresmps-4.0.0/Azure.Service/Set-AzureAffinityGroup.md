---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B2C7E454-F38F-4139-ADA2-D1C59C03CC50
online version: ''
schema: 2.0.0
ms.openlocfilehash: efa519c380ffa78f44e8ac6edebda284a4ce3cd0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967877"
---
# <span data-ttu-id="6cc32-101">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc32-101">Set-AzureAffinityGroup</span></span>

## <span data-ttu-id="6cc32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6cc32-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc32-103">修改地緣群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="6cc32-103">Modifies properties of an affinity group.</span></span>

## <span data-ttu-id="6cc32-104">句法</span><span class="sxs-lookup"><span data-stu-id="6cc32-104">SYNTAX</span></span>

```
Set-AzureAffinityGroup [-Name] <String> -Label <String> [-Description <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6cc32-105">說明</span><span class="sxs-lookup"><span data-stu-id="6cc32-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc32-106">**AzureAffinityGroup** Cmdlet 會修改 Azure 地緣群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="6cc32-106">The **Set-AzureAffinityGroup** cmdlet modifies properties of an Azure affinity group.</span></span>
<span data-ttu-id="6cc32-107">您可以變更標籤及描述。</span><span class="sxs-lookup"><span data-stu-id="6cc32-107">You can change the label and the description.</span></span>

## <span data-ttu-id="6cc32-108">示例</span><span class="sxs-lookup"><span data-stu-id="6cc32-108">EXAMPLES</span></span>

### <span data-ttu-id="6cc32-109">範例1：修改地緣群組</span><span class="sxs-lookup"><span data-stu-id="6cc32-109">Example 1: Modify an affinity group</span></span>
```
PS C:\> Set-AzureAffinityGroup -Name "South01" -Label "SouthUSProduction" -Description "Production applications for Southern US locations"
```

<span data-ttu-id="6cc32-110">這個命令會將名為 South01 的地緣群組標籤修改為 SouthUSProduction 命令也會修改描述。</span><span class="sxs-lookup"><span data-stu-id="6cc32-110">This command modifies the label of the affinity group named South01 to be SouthUSProduction The command also modifies the description.</span></span>

## <span data-ttu-id="6cc32-111">參數</span><span class="sxs-lookup"><span data-stu-id="6cc32-111">PARAMETERS</span></span>

### <span data-ttu-id="6cc32-112">-描述</span><span class="sxs-lookup"><span data-stu-id="6cc32-112">-Description</span></span>
<span data-ttu-id="6cc32-113">指定地緣群組的描述。</span><span class="sxs-lookup"><span data-stu-id="6cc32-113">Specifies the description of the affinity group.</span></span>
<span data-ttu-id="6cc32-114">描述最多可以有1024個字元。</span><span class="sxs-lookup"><span data-stu-id="6cc32-114">The description can be up to 1024 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc32-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6cc32-115">-InformationAction</span></span>
<span data-ttu-id="6cc32-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="6cc32-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6cc32-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="6cc32-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6cc32-118">持續</span><span class="sxs-lookup"><span data-stu-id="6cc32-118">Continue</span></span>
- <span data-ttu-id="6cc32-119">理會</span><span class="sxs-lookup"><span data-stu-id="6cc32-119">Ignore</span></span>
- <span data-ttu-id="6cc32-120">看</span><span class="sxs-lookup"><span data-stu-id="6cc32-120">Inquire</span></span>
- <span data-ttu-id="6cc32-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6cc32-121">SilentlyContinue</span></span>
- <span data-ttu-id="6cc32-122">停止</span><span class="sxs-lookup"><span data-stu-id="6cc32-122">Stop</span></span>
- <span data-ttu-id="6cc32-123">封存</span><span class="sxs-lookup"><span data-stu-id="6cc32-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc32-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6cc32-124">-InformationVariable</span></span>
<span data-ttu-id="6cc32-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="6cc32-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc32-126">-標籤</span><span class="sxs-lookup"><span data-stu-id="6cc32-126">-Label</span></span>
<span data-ttu-id="6cc32-127">指定地緣群組的標籤。</span><span class="sxs-lookup"><span data-stu-id="6cc32-127">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="6cc32-128">標籤可長達100個字元。</span><span class="sxs-lookup"><span data-stu-id="6cc32-128">The label can be up to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc32-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6cc32-129">-Name</span></span>
<span data-ttu-id="6cc32-130">指定此 Cmdlet 所修改之地緣群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cc32-130">Specifies the name of the affinity group that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6cc32-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6cc32-131">-Profile</span></span>
<span data-ttu-id="6cc32-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6cc32-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6cc32-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6cc32-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6cc32-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc32-134">CommonParameters</span></span>
<span data-ttu-id="6cc32-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6cc32-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc32-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6cc32-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc32-137">輸入</span><span class="sxs-lookup"><span data-stu-id="6cc32-137">INPUTS</span></span>

## <span data-ttu-id="6cc32-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6cc32-138">OUTPUTS</span></span>

## <span data-ttu-id="6cc32-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6cc32-139">NOTES</span></span>

## <span data-ttu-id="6cc32-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cc32-140">RELATED LINKS</span></span>

[<span data-ttu-id="6cc32-141">AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc32-141">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="6cc32-142">新-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc32-142">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="6cc32-143">移除-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6cc32-143">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)


