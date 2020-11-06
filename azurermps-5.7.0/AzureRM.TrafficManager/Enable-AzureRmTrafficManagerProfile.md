---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 252a633112c28b1dc1e62a6004e3f67e2b6a343a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451992"
---
# <span data-ttu-id="913d3-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="913d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="913d3-102">SYNOPSIS</span></span>
<span data-ttu-id="913d3-103">啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="913d3-104">SYNTAX</span></span>

### <span data-ttu-id="913d3-105">區域</span><span class="sxs-lookup"><span data-stu-id="913d3-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="913d3-106">面向</span><span class="sxs-lookup"><span data-stu-id="913d3-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="913d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="913d3-107">DESCRIPTION</span></span>
<span data-ttu-id="913d3-108">**Enable-AzureRmTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="913d3-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="913d3-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="913d3-110">或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="913d3-111">示例</span><span class="sxs-lookup"><span data-stu-id="913d3-111">EXAMPLES</span></span>

### <span data-ttu-id="913d3-112">範例1：啟用由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="913d3-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="913d3-113">這個命令會在 ResourceGroup11 中啟用名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="913d3-114">範例2：使用管線啟用設定檔</span><span class="sxs-lookup"><span data-stu-id="913d3-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="913d3-115">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="913d3-116">然後，命令會使用管線運算子，將該設定檔傳遞到 **Enable-AzureRmTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="913d3-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="913d3-117">該 Cmdlet 可啟用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="913d3-118">參數</span><span class="sxs-lookup"><span data-stu-id="913d3-118">PARAMETERS</span></span>

### <span data-ttu-id="913d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-119">-DefaultProfile</span></span>
<span data-ttu-id="913d3-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="913d3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="913d3-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="913d3-121">-Name</span></span>
<span data-ttu-id="913d3-122">指定此 Cmdlet 啟用的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="913d3-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="913d3-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="913d3-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="913d3-125">這個 Cmdlet 可在此參數指定的群組中啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="913d3-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913d3-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="913d3-127">指定要啟用的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="913d3-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="913d3-128">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="913d3-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913d3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913d3-129">CommonParameters</span></span>
<span data-ttu-id="913d3-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="913d3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913d3-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="913d3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913d3-132">輸入</span><span class="sxs-lookup"><span data-stu-id="913d3-132">INPUTS</span></span>

### <span data-ttu-id="913d3-133">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="913d3-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="913d3-134">這個 Cmdlet 接受 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="913d3-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="913d3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="913d3-135">OUTPUTS</span></span>

### <span data-ttu-id="913d3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="913d3-136">System.Boolean</span></span>

## <span data-ttu-id="913d3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="913d3-137">NOTES</span></span>

## <span data-ttu-id="913d3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="913d3-138">RELATED LINKS</span></span>

[<span data-ttu-id="913d3-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="913d3-140">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="913d3-141">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="913d3-142">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="913d3-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="913d3-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

