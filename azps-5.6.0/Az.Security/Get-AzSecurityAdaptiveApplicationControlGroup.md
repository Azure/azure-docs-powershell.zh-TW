---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916892"
---
# <span data-ttu-id="cc324-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="cc324-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="cc324-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc324-102">SYNOPSIS</span></span>
<span data-ttu-id="cc324-103">獲得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="cc324-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="cc324-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc324-104">SYNTAX</span></span>

### <span data-ttu-id="cc324-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="cc324-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc324-106">描述</span><span class="sxs-lookup"><span data-stu-id="cc324-106">DESCRIPTION</span></span>
<span data-ttu-id="cc324-107">自適性應用程式控制項是由 Azure 資訊安全中心自動計算，使用此 Cmdlet 取得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="cc324-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="cc324-108">例子</span><span class="sxs-lookup"><span data-stu-id="cc324-108">EXAMPLES</span></span>

### <span data-ttu-id="cc324-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="cc324-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="cc324-110">獲得應用程式控制項 VM/伺服器群組。</span><span class="sxs-lookup"><span data-stu-id="cc324-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="cc324-111">參數</span><span class="sxs-lookup"><span data-stu-id="cc324-111">PARAMETERS</span></span>

### <span data-ttu-id="cc324-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc324-112">-DefaultProfile</span></span>
<span data-ttu-id="cc324-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc324-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc324-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="cc324-114">-AscLocation</span></span>
<span data-ttu-id="cc324-115">ASC 儲存訂閱資料的位置。</span><span class="sxs-lookup"><span data-stu-id="cc324-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="cc324-116">可以從取得位置中取得。</span><span class="sxs-lookup"><span data-stu-id="cc324-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc324-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="cc324-117">-GroupName</span></span>
<span data-ttu-id="cc324-118">應用程式控制項 VM/伺服器組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc324-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc324-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc324-119">-SubscriptionId</span></span>
<span data-ttu-id="cc324-120">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc324-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="cc324-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc324-121">CommonParameters</span></span>
<span data-ttu-id="cc324-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc324-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc324-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc324-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc324-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cc324-124">INPUTS</span></span>

### <span data-ttu-id="cc324-125">System.String</span><span class="sxs-lookup"><span data-stu-id="cc324-125">System.String</span></span>

## <span data-ttu-id="cc324-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cc324-126">OUTPUTS</span></span>

### <span data-ttu-id="cc324-127">Microsoft.Azure.Commands.security.models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="cc324-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="cc324-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cc324-128">NOTES</span></span>

## <span data-ttu-id="cc324-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc324-129">RELATED LINKS</span></span>