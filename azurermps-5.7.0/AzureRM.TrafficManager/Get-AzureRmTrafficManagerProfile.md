---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451995"
---
# <span data-ttu-id="471ca-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="471ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="471ca-102">SYNOPSIS</span></span>
<span data-ttu-id="471ca-103">取得流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="471ca-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="471ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="471ca-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="471ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="471ca-105">DESCRIPTION</span></span>
<span data-ttu-id="471ca-106">**AzureRmTrafficManagerProfile** Cmdlet 會取得 Azure 流量管理器設定檔，並傳回代表該設定檔的物件。</span><span class="sxs-lookup"><span data-stu-id="471ca-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="471ca-107">依名稱和資源群組名稱來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="471ca-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="471ca-108">您可以在本機修改這個物件，然後使用 Set-AzureRmTrafficManagerProfile Cmdlet 將變更套用至設定檔。</span><span class="sxs-lookup"><span data-stu-id="471ca-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="471ca-109">示例</span><span class="sxs-lookup"><span data-stu-id="471ca-109">EXAMPLES</span></span>

### <span data-ttu-id="471ca-110">範例1：取得設定檔</span><span class="sxs-lookup"><span data-stu-id="471ca-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="471ca-111">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="471ca-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="471ca-112">參數</span><span class="sxs-lookup"><span data-stu-id="471ca-112">PARAMETERS</span></span>

### <span data-ttu-id="471ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-113">-DefaultProfile</span></span>
<span data-ttu-id="471ca-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="471ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="471ca-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="471ca-115">-Name</span></span>
<span data-ttu-id="471ca-116">指定此 Cmdlet 所取得之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="471ca-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="471ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="471ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="471ca-118">指定包含此 Cmdlet 所取得之流量管理器設定檔之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="471ca-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="471ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="471ca-119">CommonParameters</span></span>
<span data-ttu-id="471ca-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="471ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="471ca-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="471ca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="471ca-122">輸入</span><span class="sxs-lookup"><span data-stu-id="471ca-122">INPUTS</span></span>

### <span data-ttu-id="471ca-123">所有</span><span class="sxs-lookup"><span data-stu-id="471ca-123">None</span></span>
<span data-ttu-id="471ca-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="471ca-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="471ca-125">輸出</span><span class="sxs-lookup"><span data-stu-id="471ca-125">OUTPUTS</span></span>

### <span data-ttu-id="471ca-126">TrafficManagerProfile （）</span><span class="sxs-lookup"><span data-stu-id="471ca-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="471ca-127">這個 Cmdlet 會傳回 **TrafficManagerProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="471ca-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="471ca-128">您可以修改這個物件，然後使用 [ **AzureRmTrafficManagerProfile** ] 將變更套用至流量管理器。</span><span class="sxs-lookup"><span data-stu-id="471ca-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="471ca-129">筆記</span><span class="sxs-lookup"><span data-stu-id="471ca-129">NOTES</span></span>

## <span data-ttu-id="471ca-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="471ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="471ca-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="471ca-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="471ca-133">新-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="471ca-134">移除-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="471ca-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="471ca-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


