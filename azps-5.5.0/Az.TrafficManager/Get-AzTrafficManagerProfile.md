---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138139"
---
# <span data-ttu-id="7314d-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7314d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7314d-102">SYNOPSIS</span></span>
<span data-ttu-id="7314d-103">取得流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="7314d-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="7314d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7314d-104">SYNTAX</span></span>

### <span data-ttu-id="7314d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7314d-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7314d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7314d-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7314d-107">說明</span><span class="sxs-lookup"><span data-stu-id="7314d-107">DESCRIPTION</span></span>
<span data-ttu-id="7314d-108">**AzTrafficManagerProfile** Cmdlet 會取得 Azure 流量管理器設定檔，並傳回代表該設定檔的物件。</span><span class="sxs-lookup"><span data-stu-id="7314d-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="7314d-109">依名稱和資源群組名稱來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="7314d-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="7314d-110">您可以在本機修改這個物件，然後使用 Set-AzTrafficManagerProfile Cmdlet 將變更套用至設定檔。</span><span class="sxs-lookup"><span data-stu-id="7314d-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="7314d-111">示例</span><span class="sxs-lookup"><span data-stu-id="7314d-111">EXAMPLES</span></span>

### <span data-ttu-id="7314d-112">範例1：取得設定檔</span><span class="sxs-lookup"><span data-stu-id="7314d-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="7314d-113">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7314d-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="7314d-114">參數</span><span class="sxs-lookup"><span data-stu-id="7314d-114">PARAMETERS</span></span>

### <span data-ttu-id="7314d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-115">-DefaultProfile</span></span>
<span data-ttu-id="7314d-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7314d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7314d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7314d-117">-Name</span></span>
<span data-ttu-id="7314d-118">指定此 Cmdlet 所取得之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="7314d-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7314d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7314d-119">-ResourceGroupName</span></span>
<span data-ttu-id="7314d-120">指定包含此 Cmdlet 所取得之流量管理器設定檔之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7314d-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7314d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7314d-121">CommonParameters</span></span>
<span data-ttu-id="7314d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7314d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7314d-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7314d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7314d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7314d-124">INPUTS</span></span>

### <span data-ttu-id="7314d-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7314d-125">System.String</span></span>

## <span data-ttu-id="7314d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7314d-126">OUTPUTS</span></span>

### <span data-ttu-id="7314d-127">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="7314d-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7314d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7314d-128">NOTES</span></span>

## <span data-ttu-id="7314d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7314d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7314d-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7314d-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="7314d-132">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7314d-133">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="7314d-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7314d-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


