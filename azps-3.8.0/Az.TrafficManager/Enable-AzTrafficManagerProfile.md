---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957582"
---
# <span data-ttu-id="51203-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="51203-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51203-102">SYNOPSIS</span></span>
<span data-ttu-id="51203-103">啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="51203-104">句法</span><span class="sxs-lookup"><span data-stu-id="51203-104">SYNTAX</span></span>

### <span data-ttu-id="51203-105">區域</span><span class="sxs-lookup"><span data-stu-id="51203-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51203-106">面向</span><span class="sxs-lookup"><span data-stu-id="51203-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51203-107">說明</span><span class="sxs-lookup"><span data-stu-id="51203-107">DESCRIPTION</span></span>
<span data-ttu-id="51203-108">**Enable-AzTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="51203-109">您可以使用管線或參數值來指定設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="51203-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="51203-110">或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="51203-111">示例</span><span class="sxs-lookup"><span data-stu-id="51203-111">EXAMPLES</span></span>

### <span data-ttu-id="51203-112">範例1：啟用由名稱指定的設定檔</span><span class="sxs-lookup"><span data-stu-id="51203-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="51203-113">這個命令會在 ResourceGroup11 中啟用名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="51203-114">範例2：使用管線啟用設定檔</span><span class="sxs-lookup"><span data-stu-id="51203-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="51203-115">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="51203-116">然後，命令會使用管線運算子，將該設定檔傳遞到 **Enable-AzTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51203-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="51203-117">該 Cmdlet 可啟用該設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="51203-118">參數</span><span class="sxs-lookup"><span data-stu-id="51203-118">PARAMETERS</span></span>

### <span data-ttu-id="51203-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51203-119">-DefaultProfile</span></span>
<span data-ttu-id="51203-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51203-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51203-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="51203-121">-Name</span></span>
<span data-ttu-id="51203-122">指定此 Cmdlet 啟用的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="51203-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

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

### <span data-ttu-id="51203-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51203-123">-ResourceGroupName</span></span>
<span data-ttu-id="51203-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="51203-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="51203-125">這個 Cmdlet 可在此參數指定的群組中啟用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="51203-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51203-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="51203-127">指定要啟用的 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="51203-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="51203-128">若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51203-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="51203-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51203-129">CommonParameters</span></span>
<span data-ttu-id="51203-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51203-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51203-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51203-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51203-132">輸入</span><span class="sxs-lookup"><span data-stu-id="51203-132">INPUTS</span></span>

### <span data-ttu-id="51203-133">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="51203-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="51203-134">輸出</span><span class="sxs-lookup"><span data-stu-id="51203-134">OUTPUTS</span></span>

### <span data-ttu-id="51203-135">System.object</span><span class="sxs-lookup"><span data-stu-id="51203-135">System.Boolean</span></span>

## <span data-ttu-id="51203-136">筆記</span><span class="sxs-lookup"><span data-stu-id="51203-136">NOTES</span></span>

## <span data-ttu-id="51203-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="51203-137">RELATED LINKS</span></span>

[<span data-ttu-id="51203-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="51203-139">AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="51203-140">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="51203-141">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="51203-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51203-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


