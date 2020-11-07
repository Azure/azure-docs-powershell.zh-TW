---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966982"
---
# <span data-ttu-id="698aa-101">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-101">Get-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="698aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="698aa-102">SYNOPSIS</span></span>
<span data-ttu-id="698aa-103">取得流量管理器設定檔的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="698aa-103">Gets the details of a Traffic Manager profile.</span></span>

## <span data-ttu-id="698aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="698aa-104">SYNTAX</span></span>

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="698aa-105">說明</span><span class="sxs-lookup"><span data-stu-id="698aa-105">DESCRIPTION</span></span>
<span data-ttu-id="698aa-106">**AzureTrafficManagerProfile** Cmdlet 會取得 Microsoft Azure 流量管理器設定檔的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="698aa-106">The **Get-AzureTrafficManagerProfile** cmdlet gets the details of a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="698aa-107">如果您沒有指定 *Name* 參數，此 Cmdlet 會列出目前訂閱中的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="698aa-107">If you do not specify the *Name* parameter, the cmdlet lists the Traffic Manager profiles in the current subscription.</span></span>

## <span data-ttu-id="698aa-108">示例</span><span class="sxs-lookup"><span data-stu-id="698aa-108">EXAMPLES</span></span>

### <span data-ttu-id="698aa-109">範例1：取得訂閱中流量管理器設定檔的清單</span><span class="sxs-lookup"><span data-stu-id="698aa-109">Example 1: Get the list of Traffic Manager profiles in a subscription</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile
```

<span data-ttu-id="698aa-110">這個命令會在您的訂閱中取得流量管理器配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="698aa-110">This command gets the list of Traffic Manager profiles in your subscription.</span></span>

### <span data-ttu-id="698aa-111">範例2：取得流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="698aa-111">Example 2: Get a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="698aa-112">這個命令會取得名為 MyProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="698aa-112">This command gets the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="698aa-113">範例3：將端點新增至流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="698aa-113">Example 3: Add an endpoint to a Traffic Manager profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="698aa-114">這個命令會將端點新增到流量管理器設定檔，然後儲存設定檔。</span><span class="sxs-lookup"><span data-stu-id="698aa-114">This command adds an endpoint to a Traffic Manager profile, and then saves the profile.</span></span>

## <span data-ttu-id="698aa-115">參數</span><span class="sxs-lookup"><span data-stu-id="698aa-115">PARAMETERS</span></span>

### <span data-ttu-id="698aa-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="698aa-116">-Name</span></span>
<span data-ttu-id="698aa-117">指定要取得的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="698aa-117">Specifies the name of the Traffic Manager profile to get.</span></span>

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

### <span data-ttu-id="698aa-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="698aa-118">-Profile</span></span>
<span data-ttu-id="698aa-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="698aa-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="698aa-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="698aa-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="698aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="698aa-121">CommonParameters</span></span>
<span data-ttu-id="698aa-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="698aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="698aa-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="698aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="698aa-124">輸入</span><span class="sxs-lookup"><span data-stu-id="698aa-124">INPUTS</span></span>

## <span data-ttu-id="698aa-125">輸出</span><span class="sxs-lookup"><span data-stu-id="698aa-125">OUTPUTS</span></span>

### <span data-ttu-id="698aa-126">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="698aa-126">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="698aa-127">這個 Cmdlet 會產生流量管理器設定檔物件或物件。</span><span class="sxs-lookup"><span data-stu-id="698aa-127">This cmdlet generates a Traffic Manager profile object or objects.</span></span>

## <span data-ttu-id="698aa-128">筆記</span><span class="sxs-lookup"><span data-stu-id="698aa-128">NOTES</span></span>

## <span data-ttu-id="698aa-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="698aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="698aa-130">附加 AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="698aa-130">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="698aa-131">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-131">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="698aa-132">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-132">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="698aa-133">新-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-133">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="698aa-134">移除-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-134">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="698aa-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="698aa-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


