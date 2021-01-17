---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438432"
---
# <span data-ttu-id="66e3d-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="66e3d-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="66e3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="66e3d-103">建立用來建立前門的 PSBackendPoolsSetting 物件。</span><span class="sxs-lookup"><span data-stu-id="66e3d-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="66e3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="66e3d-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66e3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="66e3d-105">DESCRIPTION</span></span>
<span data-ttu-id="66e3d-106">**新的-AzFrontDoorBackendpoolsSettingObject** Cmdlet 會建立新的 PSBackendPoolsSettings 物件供前門建立。</span><span class="sxs-lookup"><span data-stu-id="66e3d-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="66e3d-107">示例</span><span class="sxs-lookup"><span data-stu-id="66e3d-107">EXAMPLES</span></span>

### <span data-ttu-id="66e3d-108">範例1：使用預設值建立 BackendPoolsSettings 物件</span><span class="sxs-lookup"><span data-stu-id="66e3d-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="66e3d-109">範例2：使用使用者指定的值建立 BackendPoolsSettings 物件</span><span class="sxs-lookup"><span data-stu-id="66e3d-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="66e3d-110">參數</span><span class="sxs-lookup"><span data-stu-id="66e3d-110">PARAMETERS</span></span>

### <span data-ttu-id="66e3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e3d-111">-DefaultProfile</span></span>
<span data-ttu-id="66e3d-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66e3d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66e3d-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="66e3d-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="66e3d-114">是否要強制對所有後端池的 HTTPS 要求進行憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="66e3d-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="66e3d-115">對非 HTTPS 式要求沒有作用。</span><span class="sxs-lookup"><span data-stu-id="66e3d-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66e3d-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="66e3d-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="66e3d-117">傳送和接收到後端的轉寄要求超時。</span><span class="sxs-lookup"><span data-stu-id="66e3d-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="66e3d-118">當達到超時時間時，要求會失敗並傳回。</span><span class="sxs-lookup"><span data-stu-id="66e3d-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="66e3d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e3d-119">CommonParameters</span></span>
<span data-ttu-id="66e3d-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66e3d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e3d-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="66e3d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e3d-122">輸入</span><span class="sxs-lookup"><span data-stu-id="66e3d-122">INPUTS</span></span>

### <span data-ttu-id="66e3d-123">所有</span><span class="sxs-lookup"><span data-stu-id="66e3d-123">None</span></span>

## <span data-ttu-id="66e3d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="66e3d-124">OUTPUTS</span></span>

### <span data-ttu-id="66e3d-125">PSBackendPoolsSetting 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="66e3d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="66e3d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="66e3d-126">NOTES</span></span>

## <span data-ttu-id="66e3d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="66e3d-127">RELATED LINKS</span></span>
