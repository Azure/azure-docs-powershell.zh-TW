---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906694"
---
# <span data-ttu-id="adc0e-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="adc0e-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="adc0e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adc0e-102">SYNOPSIS</span></span>
<span data-ttu-id="adc0e-103">建立 PSBackendPoolsSetting 物件以用於建立前門。</span><span class="sxs-lookup"><span data-stu-id="adc0e-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="adc0e-104">語法</span><span class="sxs-lookup"><span data-stu-id="adc0e-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc0e-105">描述</span><span class="sxs-lookup"><span data-stu-id="adc0e-105">DESCRIPTION</span></span>
<span data-ttu-id="adc0e-106">**New-AzFrontDoorBackendpoolsSettingObject** Cmdlet 會建立一個新的 PSBackendPoolsSettings 物件，用於建立前門。</span><span class="sxs-lookup"><span data-stu-id="adc0e-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="adc0e-107">例子</span><span class="sxs-lookup"><span data-stu-id="adc0e-107">EXAMPLES</span></span>

### <span data-ttu-id="adc0e-108">範例 1：使用預設值建立後端幕後處理物件</span><span class="sxs-lookup"><span data-stu-id="adc0e-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="adc0e-109">範例 2：使用使用者指定的值建立後端幕後處理物件</span><span class="sxs-lookup"><span data-stu-id="adc0e-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="adc0e-110">參數</span><span class="sxs-lookup"><span data-stu-id="adc0e-110">PARAMETERS</span></span>

### <span data-ttu-id="adc0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc0e-111">-DefaultProfile</span></span>
<span data-ttu-id="adc0e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adc0e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc0e-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="adc0e-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="adc0e-114">是否要針對所有後端資料庫的 HTTPS 要求強制執行憑證名稱檢查。</span><span class="sxs-lookup"><span data-stu-id="adc0e-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="adc0e-115">對非 HTTPS 要求沒有影響。</span><span class="sxs-lookup"><span data-stu-id="adc0e-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="adc0e-116">-SendRevbTimeoutIn用秒</span><span class="sxs-lookup"><span data-stu-id="adc0e-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="adc0e-117">將轉寄要求傳送及接收超時到後端。</span><span class="sxs-lookup"><span data-stu-id="adc0e-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="adc0e-118">到達超時時，要求會失敗並返回。</span><span class="sxs-lookup"><span data-stu-id="adc0e-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="adc0e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc0e-119">CommonParameters</span></span>
<span data-ttu-id="adc0e-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adc0e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc0e-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adc0e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc0e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="adc0e-122">INPUTS</span></span>

### <span data-ttu-id="adc0e-123">沒有</span><span class="sxs-lookup"><span data-stu-id="adc0e-123">None</span></span>

## <span data-ttu-id="adc0e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="adc0e-124">OUTPUTS</span></span>

### <span data-ttu-id="adc0e-125">Microsoft.Azure.Commands.FrontDoor.models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="adc0e-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="adc0e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="adc0e-126">NOTES</span></span>

## <span data-ttu-id="adc0e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc0e-127">RELATED LINKS</span></span>
