---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612365"
---
# <span data-ttu-id="9ead6-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="9ead6-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="9ead6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ead6-102">SYNOPSIS</span></span>
<span data-ttu-id="9ead6-103">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="9ead6-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9ead6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ead6-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ead6-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ead6-105">DESCRIPTION</span></span>
<span data-ttu-id="9ead6-106">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="9ead6-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9ead6-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ead6-107">EXAMPLES</span></span>

### <span data-ttu-id="9ead6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9ead6-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="9ead6-109">建立用來建立前門的 PSHealthProbeSetting 物件</span><span class="sxs-lookup"><span data-stu-id="9ead6-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="9ead6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ead6-110">PARAMETERS</span></span>

### <span data-ttu-id="9ead6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ead6-111">-DefaultProfile</span></span>
<span data-ttu-id="9ead6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ead6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ead6-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9ead6-113">-IntervalInSeconds</span></span>
<span data-ttu-id="9ead6-114">Health 探測之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="9ead6-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="9ead6-115">預設值為30</span><span class="sxs-lookup"><span data-stu-id="9ead6-115">Default value is 30</span></span>

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

### <span data-ttu-id="9ead6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ead6-116">-Name</span></span>
<span data-ttu-id="9ead6-117">health 探測設定名稱。</span><span class="sxs-lookup"><span data-stu-id="9ead6-117">health probe setting name.</span></span>

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

### <span data-ttu-id="9ead6-118">-Path</span><span class="sxs-lookup"><span data-stu-id="9ead6-118">-Path</span></span>
<span data-ttu-id="9ead6-119">要用於 health 探測的路徑。</span><span class="sxs-lookup"><span data-stu-id="9ead6-119">The path to use for the health probe.</span></span>
<span data-ttu-id="9ead6-120">預設值為/</span><span class="sxs-lookup"><span data-stu-id="9ead6-120">Default is /</span></span>

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

### <span data-ttu-id="9ead6-121">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="9ead6-121">-Protocol</span></span>
<span data-ttu-id="9ead6-122">此探針使用的通訊協定配置預設值為 HTTP</span><span class="sxs-lookup"><span data-stu-id="9ead6-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="9ead6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ead6-123">CommonParameters</span></span>
<span data-ttu-id="9ead6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ead6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ead6-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ead6-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ead6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9ead6-126">INPUTS</span></span>

### <span data-ttu-id="9ead6-127">所有</span><span class="sxs-lookup"><span data-stu-id="9ead6-127">None</span></span>

## <span data-ttu-id="9ead6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9ead6-128">OUTPUTS</span></span>

### <span data-ttu-id="9ead6-129">PSHealthProbeSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="9ead6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="9ead6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9ead6-130">NOTES</span></span>

## <span data-ttu-id="9ead6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ead6-131">RELATED LINKS</span></span>

<span data-ttu-id="9ead6-132">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="9ead6-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
