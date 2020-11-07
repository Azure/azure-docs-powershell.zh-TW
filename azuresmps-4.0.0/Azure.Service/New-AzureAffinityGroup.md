---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 54C89A5F-BF94-468C-92E7-224808FDD0EC
online version: ''
schema: 2.0.0
ms.openlocfilehash: be84995e4826b79befc6282133d70f3ee4a79b4f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967673"
---
# <span data-ttu-id="430e2-101">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="430e2-101">New-AzureAffinityGroup</span></span>

## <span data-ttu-id="430e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="430e2-102">SYNOPSIS</span></span>
<span data-ttu-id="430e2-103">在目前的訂閱中建立地緣群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-103">Creates an affinity group in the current subscription.</span></span>

## <span data-ttu-id="430e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="430e2-104">SYNTAX</span></span>

```
New-AzureAffinityGroup [-Name] <String> [-Label <String>] [-Description <String>] -Location <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="430e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="430e2-105">DESCRIPTION</span></span>
<span data-ttu-id="430e2-106">**新的-AzureAffinityGroup** Cmdlet 會在目前的 azure 訂閱中建立 Azure 地緣群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-106">The **New-AzureAffinityGroup** cmdlet creates an Azure affinity group in the current Azure subscription.</span></span>

<span data-ttu-id="430e2-107">地緣群組會將您的服務及其資源集中放在 Azure 資料中心。</span><span class="sxs-lookup"><span data-stu-id="430e2-107">An affinity group puts your services and their resources together in an Azure datacenter.</span></span>
<span data-ttu-id="430e2-108">地緣群組群組成員，以獲得最佳效能。</span><span class="sxs-lookup"><span data-stu-id="430e2-108">The affinity group groups members together for optimal performance.</span></span>
<span data-ttu-id="430e2-109">在訂閱層級定義地緣群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-109">Define affinity groups at the subscription level.</span></span>
<span data-ttu-id="430e2-110">您所建立的任何後續雲端服務或儲存空間帳戶都可使用您的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-110">Your affinity groups are available to any subsequent cloud services or storage accounts that you create.</span></span>
<span data-ttu-id="430e2-111">您只能在建立地緣群組之後，才能將服務新增至該群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-111">You can add services to an affinity group only when you create it.</span></span>

## <span data-ttu-id="430e2-112">示例</span><span class="sxs-lookup"><span data-stu-id="430e2-112">EXAMPLES</span></span>

### <span data-ttu-id="430e2-113">範例1：建立地緣群組</span><span class="sxs-lookup"><span data-stu-id="430e2-113">Example 1: Create an affinity group</span></span>
```
PS C:\> New-AzureAffinityGroup -Name "South01" -Location "South Central US" -Label "South Region" -Description "Affinity group for production applications in southern region."
```

<span data-ttu-id="430e2-114">這個命令會在美國中南部地區建立名為 South01 的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="430e2-114">This command creates an affinity group named South01 in the South Central US region.</span></span>
<span data-ttu-id="430e2-115">該命令會指定標籤和描述。</span><span class="sxs-lookup"><span data-stu-id="430e2-115">The command specifies a label and a description.</span></span>

## <span data-ttu-id="430e2-116">參數</span><span class="sxs-lookup"><span data-stu-id="430e2-116">PARAMETERS</span></span>

### <span data-ttu-id="430e2-117">-描述</span><span class="sxs-lookup"><span data-stu-id="430e2-117">-Description</span></span>
<span data-ttu-id="430e2-118">指定地緣群組的描述。</span><span class="sxs-lookup"><span data-stu-id="430e2-118">Specifies a description for the affinity group.</span></span>
<span data-ttu-id="430e2-119">描述最多可以有1024個字元。</span><span class="sxs-lookup"><span data-stu-id="430e2-119">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="430e2-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="430e2-120">-InformationAction</span></span>
<span data-ttu-id="430e2-121">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="430e2-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="430e2-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="430e2-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="430e2-123">持續</span><span class="sxs-lookup"><span data-stu-id="430e2-123">Continue</span></span>
- <span data-ttu-id="430e2-124">理會</span><span class="sxs-lookup"><span data-stu-id="430e2-124">Ignore</span></span>
- <span data-ttu-id="430e2-125">看</span><span class="sxs-lookup"><span data-stu-id="430e2-125">Inquire</span></span>
- <span data-ttu-id="430e2-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="430e2-126">SilentlyContinue</span></span>
- <span data-ttu-id="430e2-127">停止</span><span class="sxs-lookup"><span data-stu-id="430e2-127">Stop</span></span>
- <span data-ttu-id="430e2-128">封存</span><span class="sxs-lookup"><span data-stu-id="430e2-128">Suspend</span></span>

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

### <span data-ttu-id="430e2-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="430e2-129">-InformationVariable</span></span>
<span data-ttu-id="430e2-130">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="430e2-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="430e2-131">-標籤</span><span class="sxs-lookup"><span data-stu-id="430e2-131">-Label</span></span>
<span data-ttu-id="430e2-132">指定地緣群組的標籤。</span><span class="sxs-lookup"><span data-stu-id="430e2-132">Specifies a label for the affinity group.</span></span>
<span data-ttu-id="430e2-133">標籤的最大長度可能為100個字元。</span><span class="sxs-lookup"><span data-stu-id="430e2-133">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="430e2-134">-位置</span><span class="sxs-lookup"><span data-stu-id="430e2-134">-Location</span></span>
<span data-ttu-id="430e2-135">指定此 Cmdlet 建立地緣群組的 Azure 資料中心地理位置。</span><span class="sxs-lookup"><span data-stu-id="430e2-135">Specifies the geographical location of the Azure datacenter where this cmdlet creates the affinity group.</span></span>

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

### <span data-ttu-id="430e2-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="430e2-136">-Name</span></span>
<span data-ttu-id="430e2-137">指定地緣群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="430e2-137">Specifies a name for the affinity group.</span></span>
<span data-ttu-id="430e2-138">該名稱在訂閱中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="430e2-138">The name must be unique to the subscription.</span></span>

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

### <span data-ttu-id="430e2-139">-設定檔</span><span class="sxs-lookup"><span data-stu-id="430e2-139">-Profile</span></span>
<span data-ttu-id="430e2-140">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="430e2-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="430e2-141">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="430e2-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="430e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="430e2-142">CommonParameters</span></span>
<span data-ttu-id="430e2-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="430e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="430e2-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="430e2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="430e2-145">輸入</span><span class="sxs-lookup"><span data-stu-id="430e2-145">INPUTS</span></span>

## <span data-ttu-id="430e2-146">輸出</span><span class="sxs-lookup"><span data-stu-id="430e2-146">OUTPUTS</span></span>

## <span data-ttu-id="430e2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="430e2-147">NOTES</span></span>

## <span data-ttu-id="430e2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="430e2-148">RELATED LINKS</span></span>

[<span data-ttu-id="430e2-149">AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="430e2-149">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="430e2-150">移除-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="430e2-150">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="430e2-151">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="430e2-151">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


