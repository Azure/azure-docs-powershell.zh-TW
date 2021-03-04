---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: 3d843729a9ab51e5a4e1ecf1952f778537e8bf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910853"
---
# <span data-ttu-id="b3232-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="b3232-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3232-102">SYNOPSIS</span></span>
<span data-ttu-id="b3232-103">獲得流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3232-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="b3232-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3232-104">SYNTAX</span></span>

### <span data-ttu-id="b3232-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3232-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3232-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3232-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3232-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3232-107">DESCRIPTION</span></span>
<span data-ttu-id="b3232-108">**Get-AzTrafficManagerProfile** Cmdlet 會取得 Azure 流量管理員設定檔，並返回代表該設定檔的物件。</span><span class="sxs-lookup"><span data-stu-id="b3232-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="b3232-109">根據設定檔的名稱和資源組名來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3232-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="b3232-110">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzTrafficManagerProfile設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3232-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="b3232-111">例子</span><span class="sxs-lookup"><span data-stu-id="b3232-111">EXAMPLES</span></span>

### <span data-ttu-id="b3232-112">範例 1：取得設定檔</span><span class="sxs-lookup"><span data-stu-id="b3232-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="b3232-113">此命令會獲得 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3232-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="b3232-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3232-114">PARAMETERS</span></span>

### <span data-ttu-id="b3232-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-115">-DefaultProfile</span></span>
<span data-ttu-id="b3232-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3232-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3232-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3232-117">-Name</span></span>
<span data-ttu-id="b3232-118">指定此 Cmdlet 所獲得流量管理員設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3232-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3232-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3232-119">-ResourceGroupName</span></span>
<span data-ttu-id="b3232-120">指定包含此 Cmdlet 所獲得流量管理員設定檔的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3232-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3232-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3232-121">CommonParameters</span></span>
<span data-ttu-id="b3232-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3232-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3232-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b3232-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3232-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b3232-124">INPUTS</span></span>

### <span data-ttu-id="b3232-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b3232-125">System.String</span></span>

## <span data-ttu-id="b3232-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b3232-126">OUTPUTS</span></span>

### <span data-ttu-id="b3232-127">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b3232-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b3232-128">NOTES</span></span>

## <span data-ttu-id="b3232-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3232-129">RELATED LINKS</span></span>

[<span data-ttu-id="b3232-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b3232-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="b3232-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="b3232-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="b3232-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b3232-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


