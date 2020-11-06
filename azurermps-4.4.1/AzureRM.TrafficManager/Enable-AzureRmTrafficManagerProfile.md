---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 7f3849e1cabcd2fc838255bb312f5bfe5959e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450764"
---
# <span data-ttu-id="ebec1-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="ebec1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ebec1-102">SYNOPSIS</span></span>
<span data-ttu-id="ebec1-103">啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebec1-104">句法</span><span class="sxs-lookup"><span data-stu-id="ebec1-104">SYNTAX</span></span>

### <span data-ttu-id="ebec1-105">區域</span><span class="sxs-lookup"><span data-stu-id="ebec1-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebec1-106">面向</span><span class="sxs-lookup"><span data-stu-id="ebec1-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebec1-107">說明</span><span class="sxs-lookup"><span data-stu-id="ebec1-107">DESCRIPTION</span></span>
<span data-ttu-id="ebec1-108">**Enable-AzureRmTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ebec1-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ebec1-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="ebec1-110">或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="ebec1-111">示例</span><span class="sxs-lookup"><span data-stu-id="ebec1-111">EXAMPLES</span></span>

### <span data-ttu-id="ebec1-112">範例1：啟用由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="ebec1-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ebec1-113">這個命令會在 ResourceGroup11 中啟用名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="ebec1-114">範例2：使用管線啟用設定檔</span><span class="sxs-lookup"><span data-stu-id="ebec1-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="ebec1-115">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="ebec1-116">然後，命令會使用管線運算子，將該設定檔傳遞到 **Enable-AzureRmTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebec1-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebec1-117">該 Cmdlet 可啟用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="ebec1-118">參數</span><span class="sxs-lookup"><span data-stu-id="ebec1-118">PARAMETERS</span></span>

### <span data-ttu-id="ebec1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ebec1-119">-Name</span></span>
<span data-ttu-id="ebec1-120">指定此 Cmdlet 啟用的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="ebec1-120">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="ebec1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebec1-121">-ResourceGroupName</span></span>
<span data-ttu-id="ebec1-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ebec1-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ebec1-123">這個 Cmdlet 可在此參數指定的群組中啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="ebec1-123">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ebec1-124">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-124">-TrafficManagerProfile</span></span>
<span data-ttu-id="ebec1-125">指定要啟用的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebec1-125">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="ebec1-126">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebec1-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ebec1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-127">-DefaultProfile</span></span>
<span data-ttu-id="ebec1-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebec1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebec1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebec1-129">CommonParameters</span></span>
<span data-ttu-id="ebec1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ebec1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebec1-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ebec1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebec1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ebec1-132">INPUTS</span></span>

### <span data-ttu-id="ebec1-133">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="ebec1-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="ebec1-134">這個 Cmdlet 接受 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="ebec1-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="ebec1-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ebec1-135">OUTPUTS</span></span>

### <span data-ttu-id="ebec1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ebec1-136">System.Boolean</span></span>

## <span data-ttu-id="ebec1-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ebec1-137">NOTES</span></span>

## <span data-ttu-id="ebec1-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebec1-138">RELATED LINKS</span></span>

[<span data-ttu-id="ebec1-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ebec1-140">AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ebec1-141">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ebec1-142">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ebec1-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ebec1-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


