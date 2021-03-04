---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910826"
---
# <span data-ttu-id="7b1cc-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7b1cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b1cc-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1cc-103">更新流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="7b1cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b1cc-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b1cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="7b1cc-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1cc-106">**Set-AzTrafficManagerProfile** Cmdlet 會更新 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7b1cc-107">此 Cmdlet 會從本地設定檔物件更新設定檔的設定。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="7b1cc-108">您可以使用 *TrafficManagerProfile* 參數或管道來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="7b1cc-109">您可以使用 Cmdlet 取得代表設定檔的Get-AzTrafficManagerProfile物件。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7b1cc-110">在本地修改物件，然後使用 **Set-AzTrafficManagerProfile** 來提交變更。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="7b1cc-111">例子</span><span class="sxs-lookup"><span data-stu-id="7b1cc-111">EXAMPLES</span></span>

### <span data-ttu-id="7b1cc-112">範例 1：更新設定檔</span><span class="sxs-lookup"><span data-stu-id="7b1cc-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="7b1cc-113">第一個命令會使用 Get-AzTrafficManagerProfile Cmdlet 來獲得 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7b1cc-114">該命令將設定檔儲存在本地的 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="7b1cc-115">第二個命令會變更設定檔于本地。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="7b1cc-116">此命令會停用設定檔。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-116">This command disables the profile.</span></span>

<span data-ttu-id="7b1cc-117">第三個命令會更新名為 ContosoProfile 的流量管理員設定檔，以符合 $TrafficManagerProfile。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="7b1cc-118">參數</span><span class="sxs-lookup"><span data-stu-id="7b1cc-118">PARAMETERS</span></span>

### <span data-ttu-id="7b1cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-119">-DefaultProfile</span></span>
<span data-ttu-id="7b1cc-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1cc-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="7b1cc-122">指定一個本地 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7b1cc-123">此 Cmdlet 會更新流量管理員，以符合此本機物件。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="7b1cc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1cc-124">CommonParameters</span></span>
<span data-ttu-id="7b1cc-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1cc-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7b1cc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1cc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7b1cc-127">INPUTS</span></span>

### <span data-ttu-id="7b1cc-128">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7b1cc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7b1cc-129">OUTPUTS</span></span>

### <span data-ttu-id="7b1cc-130">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7b1cc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7b1cc-131">NOTES</span></span>

## <span data-ttu-id="7b1cc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b1cc-132">RELATED LINKS</span></span>

[<span data-ttu-id="7b1cc-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7b1cc-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7b1cc-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7b1cc-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7b1cc-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7b1cc-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7b1cc-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b1cc-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


