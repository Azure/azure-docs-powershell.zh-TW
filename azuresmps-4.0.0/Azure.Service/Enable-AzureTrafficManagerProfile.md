---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967821"
---
# <span data-ttu-id="d62c7-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="d62c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d62c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d62c7-103">啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d62c7-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="d62c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d62c7-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d62c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="d62c7-105">DESCRIPTION</span></span>
<span data-ttu-id="d62c7-106">**Enable-AzureTrafficManagerProfile** Cmdlet 可啟用 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d62c7-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="d62c7-107">指定 *PassThru* 參數，以顯示該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="d62c7-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="d62c7-108">示例</span><span class="sxs-lookup"><span data-stu-id="d62c7-108">EXAMPLES</span></span>

### <span data-ttu-id="d62c7-109">範例1：啟用流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="d62c7-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="d62c7-110">這個命令會啟用一個名為 MyProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="d62c7-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="d62c7-111">範例2：啟用流量管理器設定檔並顯示結果</span><span class="sxs-lookup"><span data-stu-id="d62c7-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="d62c7-112">這個命令會啟用一個名為 MyProfile 的流量管理器設定檔，並顯示該命令是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d62c7-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="d62c7-113">參數</span><span class="sxs-lookup"><span data-stu-id="d62c7-113">PARAMETERS</span></span>

### <span data-ttu-id="d62c7-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="d62c7-114">-Name</span></span>
<span data-ttu-id="d62c7-115">指定要啟用的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="d62c7-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="d62c7-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d62c7-116">-PassThru</span></span>
<span data-ttu-id="d62c7-117">如果操作成功，則傳回 $True;否則，請 $False。</span><span class="sxs-lookup"><span data-stu-id="d62c7-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="d62c7-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d62c7-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d62c7-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d62c7-119">-Profile</span></span>
<span data-ttu-id="d62c7-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d62c7-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d62c7-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d62c7-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d62c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62c7-122">CommonParameters</span></span>
<span data-ttu-id="d62c7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d62c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62c7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d62c7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62c7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d62c7-125">INPUTS</span></span>

## <span data-ttu-id="d62c7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d62c7-126">OUTPUTS</span></span>

### <span data-ttu-id="d62c7-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d62c7-127">System.Boolean</span></span>
<span data-ttu-id="d62c7-128">這個 Cmdlet 會產生 $True 或 $False。</span><span class="sxs-lookup"><span data-stu-id="d62c7-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="d62c7-129">如果操作成功且您指定 *PassThru* 參數，則此 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="d62c7-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="d62c7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d62c7-130">NOTES</span></span>

## <span data-ttu-id="d62c7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d62c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="d62c7-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d62c7-133">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d62c7-134">新-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d62c7-135">移除-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="d62c7-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d62c7-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


