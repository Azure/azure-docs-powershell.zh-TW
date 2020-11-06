---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: fe97e35c0b4b728601cc33888deb9afbdb0620b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614345"
---
# <span data-ttu-id="97799-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="97799-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97799-102">SYNOPSIS</span></span>
<span data-ttu-id="97799-103">取得流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="97799-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="97799-104">句法</span><span class="sxs-lookup"><span data-stu-id="97799-104">SYNTAX</span></span>

### <span data-ttu-id="97799-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="97799-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97799-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="97799-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97799-107">說明</span><span class="sxs-lookup"><span data-stu-id="97799-107">DESCRIPTION</span></span>
<span data-ttu-id="97799-108">**AzTrafficManagerProfile** Cmdlet 會取得 Azure 流量管理器設定檔，並傳回代表該設定檔的物件。</span><span class="sxs-lookup"><span data-stu-id="97799-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="97799-109">依名稱和資源群組名稱來指定設定檔。</span><span class="sxs-lookup"><span data-stu-id="97799-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="97799-110">您可以在本機修改這個物件，然後使用 Set-AzTrafficManagerProfile Cmdlet 將變更套用至設定檔。</span><span class="sxs-lookup"><span data-stu-id="97799-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="97799-111">示例</span><span class="sxs-lookup"><span data-stu-id="97799-111">EXAMPLES</span></span>

### <span data-ttu-id="97799-112">範例1：取得設定檔</span><span class="sxs-lookup"><span data-stu-id="97799-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="97799-113">這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="97799-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="97799-114">參數</span><span class="sxs-lookup"><span data-stu-id="97799-114">PARAMETERS</span></span>

### <span data-ttu-id="97799-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97799-115">-DefaultProfile</span></span>
<span data-ttu-id="97799-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97799-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97799-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="97799-117">-Name</span></span>
<span data-ttu-id="97799-118">指定此 Cmdlet 所取得之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="97799-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97799-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97799-119">-ResourceGroupName</span></span>
<span data-ttu-id="97799-120">指定包含此 Cmdlet 所取得之流量管理器設定檔之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97799-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97799-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97799-121">CommonParameters</span></span>
<span data-ttu-id="97799-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97799-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97799-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97799-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97799-124">輸入</span><span class="sxs-lookup"><span data-stu-id="97799-124">INPUTS</span></span>

### <span data-ttu-id="97799-125">System.object</span><span class="sxs-lookup"><span data-stu-id="97799-125">System.String</span></span>

## <span data-ttu-id="97799-126">輸出</span><span class="sxs-lookup"><span data-stu-id="97799-126">OUTPUTS</span></span>

### <span data-ttu-id="97799-127">TrafficManagerProfile 中的 TrafficManager。</span><span class="sxs-lookup"><span data-stu-id="97799-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="97799-128">筆記</span><span class="sxs-lookup"><span data-stu-id="97799-128">NOTES</span></span>

## <span data-ttu-id="97799-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="97799-129">RELATED LINKS</span></span>

[<span data-ttu-id="97799-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="97799-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="97799-132">新-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="97799-133">移除-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="97799-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="97799-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


