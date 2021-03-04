---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: 40bfe0d68df65b7535ec40a3cb27da1501f915c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910862"
---
# <span data-ttu-id="4b19d-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="4b19d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b19d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b19d-103">啟用流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="4b19d-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b19d-104">SYNTAX</span></span>

### <span data-ttu-id="4b19d-105">領域</span><span class="sxs-lookup"><span data-stu-id="4b19d-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b19d-106">物件</span><span class="sxs-lookup"><span data-stu-id="4b19d-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b19d-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b19d-107">DESCRIPTION</span></span>
<span data-ttu-id="4b19d-108">**Enable-AzTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4b19d-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="4b19d-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="4b19d-110">或者，您可以使用 Name 和 *ResourceGroupName* 參數來指定設定檔。 </span><span class="sxs-lookup"><span data-stu-id="4b19d-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="4b19d-111">例子</span><span class="sxs-lookup"><span data-stu-id="4b19d-111">EXAMPLES</span></span>

### <span data-ttu-id="4b19d-112">範例 1：啟用由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="4b19d-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="4b19d-113">此命令會啟用 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="4b19d-114">範例 2：使用管線啟用設定檔</span><span class="sxs-lookup"><span data-stu-id="4b19d-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="4b19d-115">此命令會獲得 ResourceGroup11 中名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="4b19d-116">命令接著使用管線運算子，將設定檔傳遞至 **Enable-AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b19d-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b19d-117">該 Cmdlet 會啟用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="4b19d-118">參數</span><span class="sxs-lookup"><span data-stu-id="4b19d-118">PARAMETERS</span></span>

### <span data-ttu-id="4b19d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-119">-DefaultProfile</span></span>
<span data-ttu-id="4b19d-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b19d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b19d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b19d-121">-Name</span></span>
<span data-ttu-id="4b19d-122">指定此 Cmdlet 啟用的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="4b19d-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b19d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b19d-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b19d-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b19d-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4b19d-125">此 Cmdlet 會啟用此參數指定之群組中的流量管理員設定檔。</span><span class="sxs-lookup"><span data-stu-id="4b19d-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b19d-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="4b19d-127">指定 **要啟用的 TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="4b19d-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="4b19d-128">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b19d-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b19d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b19d-129">CommonParameters</span></span>
<span data-ttu-id="4b19d-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b19d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b19d-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4b19d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b19d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4b19d-132">INPUTS</span></span>

### <span data-ttu-id="4b19d-133">Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4b19d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4b19d-134">OUTPUTS</span></span>

### <span data-ttu-id="4b19d-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b19d-135">System.Boolean</span></span>

## <span data-ttu-id="4b19d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4b19d-136">NOTES</span></span>

## <span data-ttu-id="4b19d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b19d-137">RELATED LINKS</span></span>

[<span data-ttu-id="4b19d-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="4b19d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4b19d-140">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="4b19d-141">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="4b19d-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4b19d-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


