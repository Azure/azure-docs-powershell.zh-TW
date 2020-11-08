---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRKey.md
ms.openlocfilehash: e71795c04d421ad0c6772ddd23724b5d53d38e86
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129231"
---
# <span data-ttu-id="5b215-101">Get-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="5b215-101">Get-AzSignalRKey</span></span>

## <span data-ttu-id="5b215-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b215-102">SYNOPSIS</span></span>
<span data-ttu-id="5b215-103">取得 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b215-103">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5b215-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b215-104">SYNTAX</span></span>

### <span data-ttu-id="5b215-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5b215-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b215-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b215-106">ResourceIdParameterSet</span></span>
```
Get-AzSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b215-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b215-107">InputObjectParameterSet</span></span>
```
Get-AzSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b215-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b215-108">DESCRIPTION</span></span>
<span data-ttu-id="5b215-109">取得 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5b215-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="5b215-110">示例</span><span class="sxs-lookup"><span data-stu-id="5b215-110">EXAMPLES</span></span>

### <span data-ttu-id="5b215-111">取得特定 SignalR 服務的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="5b215-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="5b215-112">從管道中的 SignalR 服務物件取得便捷鍵</span><span class="sxs-lookup"><span data-stu-id="5b215-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="5b215-113">參數</span><span class="sxs-lookup"><span data-stu-id="5b215-113">PARAMETERS</span></span>

### <span data-ttu-id="5b215-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b215-114">-DefaultProfile</span></span>
<span data-ttu-id="5b215-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b215-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b215-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b215-116">-InputObject</span></span>
<span data-ttu-id="5b215-117">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="5b215-117">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b215-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b215-118">-Name</span></span>
<span data-ttu-id="5b215-119">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="5b215-119">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b215-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b215-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b215-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5b215-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b215-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b215-122">-ResourceId</span></span>
<span data-ttu-id="5b215-123">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b215-123">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b215-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b215-124">CommonParameters</span></span>
<span data-ttu-id="5b215-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b215-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b215-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b215-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b215-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5b215-127">INPUTS</span></span>

### <span data-ttu-id="5b215-128">System.object</span><span class="sxs-lookup"><span data-stu-id="5b215-128">System.String</span></span>
### <span data-ttu-id="5b215-129">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="5b215-129">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="5b215-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5b215-130">OUTPUTS</span></span>

### <span data-ttu-id="5b215-131">PSSignalRKeys 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="5b215-131">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>
## <span data-ttu-id="5b215-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5b215-132">NOTES</span></span>

## <span data-ttu-id="5b215-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b215-133">RELATED LINKS</span></span>