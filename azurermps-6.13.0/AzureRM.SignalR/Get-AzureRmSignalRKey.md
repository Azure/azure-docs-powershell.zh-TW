---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Get-AzureRmSignalRKey.md
ms.openlocfilehash: 3eaef21cc9652ee7e5e4c52a51bcc3ab8bd5b1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624160"
---
# <span data-ttu-id="4a80f-101">Get-AzureRmSignalRKey</span><span class="sxs-lookup"><span data-stu-id="4a80f-101">Get-AzureRmSignalRKey</span></span>

## <span data-ttu-id="4a80f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a80f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a80f-103">取得 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4a80f-103">Get the access keys of a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a80f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a80f-104">SYNTAX</span></span>

### <span data-ttu-id="4a80f-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4a80f-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a80f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a80f-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSignalRKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a80f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a80f-107">InputObjectParameterSet</span></span>
```
Get-AzureRmSignalRKey -InputObject <PSSignalRResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a80f-108">說明</span><span class="sxs-lookup"><span data-stu-id="4a80f-108">DESCRIPTION</span></span>
<span data-ttu-id="4a80f-109">取得 SignalR 服務的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="4a80f-109">Get the access keys of a SignalR service.</span></span>

## <span data-ttu-id="4a80f-110">示例</span><span class="sxs-lookup"><span data-stu-id="4a80f-110">EXAMPLES</span></span>

### <span data-ttu-id="4a80f-111">取得特定 SignalR 服務的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="4a80f-111">Get access keys of a specific SignalR service</span></span>
```powershell
PS C:\> Get-AzureRmSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

### <span data-ttu-id="4a80f-112">從管道中的 SignalR 服務物件取得便捷鍵</span><span class="sxs-lookup"><span data-stu-id="4a80f-112">Get access keys from a SignalR service object in pipe</span></span>

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 | Get-AzureRmSignalRKey

Name                      : mysignalr1
PrimaryKey                : vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmOQNt77PovDs=
PrimaryConnectionString   : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=vmYRhoM62PMkNe/CSSPdMSxokn+WZEFmO
                            QNt77PovDs=;
SecondaryKey              : 2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsdXSjN4C/YFQ=
SecondaryConnectionString : Endpoint=https://mysignalr1.service.signalr.net;AccessKey=2+HkuxAA34xiZFFiDsVM0uDyzCsg6GKsd
                            XSjN4C/YFQ=;
```

## <span data-ttu-id="4a80f-113">參數</span><span class="sxs-lookup"><span data-stu-id="4a80f-113">PARAMETERS</span></span>

### <span data-ttu-id="4a80f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a80f-114">-DefaultProfile</span></span>
<span data-ttu-id="4a80f-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4a80f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a80f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a80f-116">-InputObject</span></span>
<span data-ttu-id="4a80f-117">SignalR 資源物件。</span><span class="sxs-lookup"><span data-stu-id="4a80f-117">The SignalR resource object.</span></span>

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

### <span data-ttu-id="4a80f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a80f-118">-Name</span></span>
<span data-ttu-id="4a80f-119">SignalR 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="4a80f-119">SignalR service name.</span></span>

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

### <span data-ttu-id="4a80f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a80f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a80f-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4a80f-121">Resource group name.</span></span>

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

### <span data-ttu-id="4a80f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a80f-122">-ResourceId</span></span>
<span data-ttu-id="4a80f-123">SignalR 服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a80f-123">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="4a80f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a80f-124">CommonParameters</span></span>
<span data-ttu-id="4a80f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a80f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a80f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a80f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a80f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4a80f-127">INPUTS</span></span>

### <span data-ttu-id="4a80f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4a80f-128">System.String</span></span>
<span data-ttu-id="4a80f-129">參數： ResourceId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4a80f-129">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="4a80f-130">PSSignalRResource 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="4a80f-130">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="4a80f-131">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4a80f-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4a80f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4a80f-132">OUTPUTS</span></span>

### <span data-ttu-id="4a80f-133">PSSignalRKeys 中的 SignalR。</span><span class="sxs-lookup"><span data-stu-id="4a80f-133">Microsoft.Azure.Commands.SignalR.Models.PSSignalRKeys</span></span>

## <span data-ttu-id="4a80f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4a80f-134">NOTES</span></span>

## <span data-ttu-id="4a80f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a80f-135">RELATED LINKS</span></span>
