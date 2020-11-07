---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967618"
---
# <span data-ttu-id="a1c24-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c24-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="a1c24-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1c24-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c24-103">刪除訂閱中的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="a1c24-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="a1c24-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1c24-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a1c24-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1c24-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c24-106">**AzureAffinityGroup** Cmdlet 會刪除目前訂閱中的 Azure 地緣群組。</span><span class="sxs-lookup"><span data-stu-id="a1c24-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="a1c24-107">您無法刪除擁有任何成員的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="a1c24-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="a1c24-108">您必須先刪除地緣群組的所有成員。</span><span class="sxs-lookup"><span data-stu-id="a1c24-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="a1c24-109">示例</span><span class="sxs-lookup"><span data-stu-id="a1c24-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c24-110">範例1：移除地緣群組</span><span class="sxs-lookup"><span data-stu-id="a1c24-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="a1c24-111">這個命令會刪除目前訂閱中的 South01 親近性群組。</span><span class="sxs-lookup"><span data-stu-id="a1c24-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="a1c24-112">參數</span><span class="sxs-lookup"><span data-stu-id="a1c24-112">PARAMETERS</span></span>

### <span data-ttu-id="a1c24-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a1c24-113">-InformationAction</span></span>
<span data-ttu-id="a1c24-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a1c24-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a1c24-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1c24-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c24-116">持續</span><span class="sxs-lookup"><span data-stu-id="a1c24-116">Continue</span></span>
- <span data-ttu-id="a1c24-117">理會</span><span class="sxs-lookup"><span data-stu-id="a1c24-117">Ignore</span></span>
- <span data-ttu-id="a1c24-118">看</span><span class="sxs-lookup"><span data-stu-id="a1c24-118">Inquire</span></span>
- <span data-ttu-id="a1c24-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a1c24-119">SilentlyContinue</span></span>
- <span data-ttu-id="a1c24-120">停止</span><span class="sxs-lookup"><span data-stu-id="a1c24-120">Stop</span></span>
- <span data-ttu-id="a1c24-121">封存</span><span class="sxs-lookup"><span data-stu-id="a1c24-121">Suspend</span></span>

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

### <span data-ttu-id="a1c24-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a1c24-122">-InformationVariable</span></span>
<span data-ttu-id="a1c24-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a1c24-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a1c24-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1c24-124">-Name</span></span>
<span data-ttu-id="a1c24-125">指定此 Cmdlet 刪除之地緣群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1c24-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a1c24-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a1c24-126">-Profile</span></span>
<span data-ttu-id="a1c24-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a1c24-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1c24-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a1c24-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1c24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c24-129">CommonParameters</span></span>
<span data-ttu-id="a1c24-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1c24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c24-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1c24-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c24-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a1c24-132">INPUTS</span></span>

## <span data-ttu-id="a1c24-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a1c24-133">OUTPUTS</span></span>

## <span data-ttu-id="a1c24-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a1c24-134">NOTES</span></span>

## <span data-ttu-id="a1c24-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1c24-135">RELATED LINKS</span></span>

[<span data-ttu-id="a1c24-136">AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c24-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="a1c24-137">新-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c24-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="a1c24-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c24-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


