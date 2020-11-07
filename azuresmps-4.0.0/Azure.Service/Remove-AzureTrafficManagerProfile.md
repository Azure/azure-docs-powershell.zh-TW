---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967537"
---
# <span data-ttu-id="575d6-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="575d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="575d6-102">SYNOPSIS</span></span>
<span data-ttu-id="575d6-103">移除流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="575d6-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="575d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="575d6-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="575d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="575d6-105">DESCRIPTION</span></span>
<span data-ttu-id="575d6-106">**AzureTrafficManagerProfile** Cmdlet 會從目前的訂閱中移除 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="575d6-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="575d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="575d6-107">EXAMPLES</span></span>

### <span data-ttu-id="575d6-108">範例1：移除流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="575d6-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="575d6-109">這個命令會移除名為 MyProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="575d6-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="575d6-110">範例2：移除流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="575d6-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="575d6-111">這個命令會移除名為 MyProfile 的流量管理器設定檔，而不會提示您確認，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="575d6-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="575d6-112">參數</span><span class="sxs-lookup"><span data-stu-id="575d6-112">PARAMETERS</span></span>

### <span data-ttu-id="575d6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="575d6-113">-Force</span></span>
<span data-ttu-id="575d6-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="575d6-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575d6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="575d6-115">-Name</span></span>
<span data-ttu-id="575d6-116">指定要刪除的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="575d6-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="575d6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="575d6-117">-PassThru</span></span>
<span data-ttu-id="575d6-118">如果操作成功，則傳回 $True;否則，請 $False。</span><span class="sxs-lookup"><span data-stu-id="575d6-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="575d6-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="575d6-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="575d6-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="575d6-120">-Profile</span></span>
<span data-ttu-id="575d6-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="575d6-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="575d6-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="575d6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="575d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575d6-123">CommonParameters</span></span>
<span data-ttu-id="575d6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="575d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575d6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="575d6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575d6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="575d6-126">INPUTS</span></span>

## <span data-ttu-id="575d6-127">輸出</span><span class="sxs-lookup"><span data-stu-id="575d6-127">OUTPUTS</span></span>

### <span data-ttu-id="575d6-128">System.object</span><span class="sxs-lookup"><span data-stu-id="575d6-128">System.Boolean</span></span>
<span data-ttu-id="575d6-129">這個 Cmdlet 會產生 $True 或 $False。</span><span class="sxs-lookup"><span data-stu-id="575d6-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="575d6-130">如果操作成功，且您指定 *PassThru* 參數，則此 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="575d6-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="575d6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="575d6-131">NOTES</span></span>

## <span data-ttu-id="575d6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="575d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="575d6-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="575d6-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="575d6-135">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="575d6-136">新-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="575d6-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="575d6-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


