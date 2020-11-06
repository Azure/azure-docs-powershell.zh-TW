---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449169"
---
# <span data-ttu-id="48b0a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="48b0a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="48b0a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48b0a-102">SYNOPSIS</span></span>
<span data-ttu-id="48b0a-103">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="48b0a-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b0a-104">句法</span><span class="sxs-lookup"><span data-stu-id="48b0a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b0a-105">說明</span><span class="sxs-lookup"><span data-stu-id="48b0a-105">DESCRIPTION</span></span>
<span data-ttu-id="48b0a-106">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="48b0a-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="48b0a-107">示例</span><span class="sxs-lookup"><span data-stu-id="48b0a-107">EXAMPLES</span></span>

### <span data-ttu-id="48b0a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="48b0a-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="48b0a-109">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="48b0a-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="48b0a-110">參數</span><span class="sxs-lookup"><span data-stu-id="48b0a-110">PARAMETERS</span></span>

### <span data-ttu-id="48b0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b0a-111">-DefaultProfile</span></span>
<span data-ttu-id="48b0a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48b0a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b0a-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="48b0a-113">-IntervalInSeconds</span></span>
<span data-ttu-id="48b0a-114">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="48b0a-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="48b0a-115">預設值為30</span><span class="sxs-lookup"><span data-stu-id="48b0a-115">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b0a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="48b0a-116">-Name</span></span>
<span data-ttu-id="48b0a-117">health 探測設定名稱。</span><span class="sxs-lookup"><span data-stu-id="48b0a-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b0a-118">-Path</span><span class="sxs-lookup"><span data-stu-id="48b0a-118">-Path</span></span>
<span data-ttu-id="48b0a-119">要用於 health 探測的路徑。</span><span class="sxs-lookup"><span data-stu-id="48b0a-119">The path to use for the health probe.</span></span>
<span data-ttu-id="48b0a-120">預設值為/</span><span class="sxs-lookup"><span data-stu-id="48b0a-120">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b0a-121">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="48b0a-121">-Protocol</span></span>
<span data-ttu-id="48b0a-122">此探針使用的通訊協定配置預設值為 HTTP</span><span class="sxs-lookup"><span data-stu-id="48b0a-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b0a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b0a-123">CommonParameters</span></span>
<span data-ttu-id="48b0a-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48b0a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b0a-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48b0a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b0a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="48b0a-126">INPUTS</span></span>

### <span data-ttu-id="48b0a-127">所有</span><span class="sxs-lookup"><span data-stu-id="48b0a-127">None</span></span>

## <span data-ttu-id="48b0a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="48b0a-128">OUTPUTS</span></span>

### <span data-ttu-id="48b0a-129">PSHealthProbeSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="48b0a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="48b0a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="48b0a-130">NOTES</span></span>

## <span data-ttu-id="48b0a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="48b0a-131">RELATED LINKS</span></span>

<span data-ttu-id="48b0a-132">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="48b0a-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
