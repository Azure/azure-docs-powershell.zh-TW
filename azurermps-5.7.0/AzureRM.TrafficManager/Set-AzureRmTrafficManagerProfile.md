---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452959"
---
# <span data-ttu-id="8e27a-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="8e27a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e27a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e27a-103">更新流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e27a-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e27a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e27a-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e27a-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e27a-105">DESCRIPTION</span></span>
<span data-ttu-id="8e27a-106">**AzureRmTrafficManagerProfile** Cmdlet 會更新 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e27a-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8e27a-107">這個 Cmdlet 會從本機設定檔物件更新設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="8e27a-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="8e27a-108">您可以使用 *TrafficManagerProfile* 參數或使用管線來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="8e27a-109">您可以使用 Get-AzureRmTrafficManagerProfile Cmdlet 來取得代表設定檔的局部物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="8e27a-110">在本機修改物件，然後使用 [ **設定] AzureRmTrafficManagerProfile** 來認可您的變更。</span><span class="sxs-lookup"><span data-stu-id="8e27a-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="8e27a-111">示例</span><span class="sxs-lookup"><span data-stu-id="8e27a-111">EXAMPLES</span></span>

### <span data-ttu-id="8e27a-112">範例1：更新設定檔</span><span class="sxs-lookup"><span data-stu-id="8e27a-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="8e27a-113">第一個命令會使用 Get-AzureRmTrafficManagerProfile Cmdlet 來取得 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e27a-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="8e27a-114">該命令會將設定檔儲存在本機 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e27a-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="8e27a-115">第二個命令會在本機變更該設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e27a-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="8e27a-116">這個命令會停用設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e27a-116">This command disables the profile.</span></span>

<span data-ttu-id="8e27a-117">第三個命令會更新名為 ContosoProfile 的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。</span><span class="sxs-lookup"><span data-stu-id="8e27a-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="8e27a-118">參數</span><span class="sxs-lookup"><span data-stu-id="8e27a-118">PARAMETERS</span></span>

### <span data-ttu-id="8e27a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-119">-DefaultProfile</span></span>
<span data-ttu-id="8e27a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e27a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e27a-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="8e27a-122">指定本機 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="8e27a-123">這個 Cmdlet 會更新流量管理器，以符合這個本機物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e27a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e27a-124">CommonParameters</span></span>
<span data-ttu-id="8e27a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e27a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e27a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e27a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e27a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8e27a-127">INPUTS</span></span>

### <span data-ttu-id="8e27a-128">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="8e27a-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8e27a-129">這個 Cmdlet 接受 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="8e27a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8e27a-130">OUTPUTS</span></span>

### <span data-ttu-id="8e27a-131">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="8e27a-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8e27a-132">這個 Cmdlet 會傳回 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e27a-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="8e27a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8e27a-133">NOTES</span></span>

## <span data-ttu-id="8e27a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e27a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8e27a-135">附加 AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8e27a-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="8e27a-136">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8e27a-137">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8e27a-138">移除-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8e27a-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="8e27a-139">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8e27a-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


