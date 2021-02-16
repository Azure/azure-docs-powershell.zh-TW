---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133583"
---
# <span data-ttu-id="45621-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="45621-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="45621-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45621-102">SYNOPSIS</span></span>
<span data-ttu-id="45621-103">在 Azure 安全中心中取得安全性設定</span><span class="sxs-lookup"><span data-stu-id="45621-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="45621-104">句法</span><span class="sxs-lookup"><span data-stu-id="45621-104">SYNTAX</span></span>

### <span data-ttu-id="45621-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="45621-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45621-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="45621-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45621-107">說明</span><span class="sxs-lookup"><span data-stu-id="45621-107">DESCRIPTION</span></span>
<span data-ttu-id="45621-108">Get-AzSecuritySetting Cmdlet 會取得 Azure 安全中心中的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="45621-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="45621-109">示例</span><span class="sxs-lookup"><span data-stu-id="45621-109">EXAMPLES</span></span>

### <span data-ttu-id="45621-110">範例1</span><span class="sxs-lookup"><span data-stu-id="45621-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="45621-111">取得 MCAS 資料匯出設定</span><span class="sxs-lookup"><span data-stu-id="45621-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="45621-112">參數</span><span class="sxs-lookup"><span data-stu-id="45621-112">PARAMETERS</span></span>

### <span data-ttu-id="45621-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45621-113">-DefaultProfile</span></span>
<span data-ttu-id="45621-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45621-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45621-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="45621-115">-SettingName</span></span>
<span data-ttu-id="45621-116">設定名稱。</span><span class="sxs-lookup"><span data-stu-id="45621-116">Setting name.</span></span> <span data-ttu-id="45621-117"> (MCAS/WDATP) </span><span class="sxs-lookup"><span data-stu-id="45621-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="45621-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45621-118">CommonParameters</span></span>
<span data-ttu-id="45621-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45621-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45621-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45621-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45621-121">輸入</span><span class="sxs-lookup"><span data-stu-id="45621-121">INPUTS</span></span>

### <span data-ttu-id="45621-122">System.object</span><span class="sxs-lookup"><span data-stu-id="45621-122">System.String</span></span>

## <span data-ttu-id="45621-123">輸出</span><span class="sxs-lookup"><span data-stu-id="45621-123">OUTPUTS</span></span>

### <span data-ttu-id="45621-124">PSSecuritySetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="45621-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="45621-125">PSSecurityDataExportSetting （Security. 命令。</span><span class="sxs-lookup"><span data-stu-id="45621-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="45621-126">筆記</span><span class="sxs-lookup"><span data-stu-id="45621-126">NOTES</span></span>

## <span data-ttu-id="45621-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="45621-127">RELATED LINKS</span></span>
