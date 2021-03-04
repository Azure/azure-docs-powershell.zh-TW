---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906858"
---
# <span data-ttu-id="ef850-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ef850-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="ef850-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef850-102">SYNOPSIS</span></span>
<span data-ttu-id="ef850-103">在 Azure 資訊安全中心中取得安全性設定</span><span class="sxs-lookup"><span data-stu-id="ef850-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="ef850-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef850-104">SYNTAX</span></span>

### <span data-ttu-id="ef850-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ef850-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef850-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ef850-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef850-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef850-107">DESCRIPTION</span></span>
<span data-ttu-id="ef850-108">Cmdlet Get-AzSecuritySetting Azure 資訊安全中心中取得安全性設定。</span><span class="sxs-lookup"><span data-stu-id="ef850-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="ef850-109">例子</span><span class="sxs-lookup"><span data-stu-id="ef850-109">EXAMPLES</span></span>

### <span data-ttu-id="ef850-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ef850-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="ef850-111">獲得 MCAS 資料匯出設定</span><span class="sxs-lookup"><span data-stu-id="ef850-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="ef850-112">參數</span><span class="sxs-lookup"><span data-stu-id="ef850-112">PARAMETERS</span></span>

### <span data-ttu-id="ef850-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef850-113">-DefaultProfile</span></span>
<span data-ttu-id="ef850-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef850-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef850-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="ef850-115">-SettingName</span></span>
<span data-ttu-id="ef850-116">設定名稱。</span><span class="sxs-lookup"><span data-stu-id="ef850-116">Setting name.</span></span> <span data-ttu-id="ef850-117"> (MCAS/WDATP) </span><span class="sxs-lookup"><span data-stu-id="ef850-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef850-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef850-118">CommonParameters</span></span>
<span data-ttu-id="ef850-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef850-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef850-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef850-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef850-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ef850-121">INPUTS</span></span>

### <span data-ttu-id="ef850-122">System.String</span><span class="sxs-lookup"><span data-stu-id="ef850-122">System.String</span></span>

## <span data-ttu-id="ef850-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ef850-123">OUTPUTS</span></span>

### <span data-ttu-id="ef850-124">Microsoft.Azure.Commands.security.models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="ef850-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="ef850-125">Microsoft.Azure.Commands.security.models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="ef850-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="ef850-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ef850-126">NOTES</span></span>

## <span data-ttu-id="ef850-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef850-127">RELATED LINKS</span></span>
