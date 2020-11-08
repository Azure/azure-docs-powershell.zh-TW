---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129384"
---
# <span data-ttu-id="96b4c-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="96b4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="96b4c-103">更新流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="96b4c-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="96b4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="96b4c-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96b4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="96b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="96b4c-106">**AzTrafficManagerProfile** Cmdlet 會更新 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="96b4c-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="96b4c-107">這個 Cmdlet 會從本機設定檔物件更新設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="96b4c-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="96b4c-108">您可以使用 *TrafficManagerProfile* 參數或使用管線來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="96b4c-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="96b4c-109">您可以使用 Get-AzTrafficManagerProfile Cmdlet 來取得代表設定檔的局部物件。</span><span class="sxs-lookup"><span data-stu-id="96b4c-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="96b4c-110">在本機修改物件，然後使用 [ **設定] AzTrafficManagerProfile** 來認可您的變更。</span><span class="sxs-lookup"><span data-stu-id="96b4c-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="96b4c-111">示例</span><span class="sxs-lookup"><span data-stu-id="96b4c-111">EXAMPLES</span></span>

### <span data-ttu-id="96b4c-112">範例1：更新設定檔</span><span class="sxs-lookup"><span data-stu-id="96b4c-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="96b4c-113">第一個命令會使用 Get-AzTrafficManagerProfile Cmdlet 來取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="96b4c-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="96b4c-114">該命令會將設定檔儲存在本機 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="96b4c-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="96b4c-115">第二個命令會在本機變更該設定檔。</span><span class="sxs-lookup"><span data-stu-id="96b4c-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="96b4c-116">這個命令會停用設定檔。</span><span class="sxs-lookup"><span data-stu-id="96b4c-116">This command disables the profile.</span></span>

<span data-ttu-id="96b4c-117">第三個命令會更新名為 ContosoProfile 的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="96b4c-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="96b4c-118">參數</span><span class="sxs-lookup"><span data-stu-id="96b4c-118">PARAMETERS</span></span>

### <span data-ttu-id="96b4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-119">-DefaultProfile</span></span>
<span data-ttu-id="96b4c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96b4c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96b4c-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="96b4c-122">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="96b4c-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="96b4c-123">這個 Cmdlet 會更新流量管理器，以符合這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="96b4c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96b4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b4c-124">CommonParameters</span></span>
<span data-ttu-id="96b4c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96b4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b4c-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96b4c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b4c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="96b4c-127">INPUTS</span></span>

### <span data-ttu-id="96b4c-128">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="96b4c-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="96b4c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="96b4c-129">OUTPUTS</span></span>

### <span data-ttu-id="96b4c-130">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="96b4c-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="96b4c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="96b4c-131">NOTES</span></span>

## <span data-ttu-id="96b4c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="96b4c-132">RELATED LINKS</span></span>

[<span data-ttu-id="96b4c-133">附加 AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="96b4c-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="96b4c-134">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="96b4c-135">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="96b4c-136">移除-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="96b4c-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="96b4c-137">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96b4c-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

