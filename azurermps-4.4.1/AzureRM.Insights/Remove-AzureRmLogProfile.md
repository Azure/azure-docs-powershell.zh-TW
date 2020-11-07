---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624815"
---
# <span data-ttu-id="939e5-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="939e5-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="939e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="939e5-102">SYNOPSIS</span></span>
<span data-ttu-id="939e5-103">移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="939e5-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="939e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="939e5-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="939e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="939e5-105">DESCRIPTION</span></span>
<span data-ttu-id="939e5-106">**AzureRmLogProfile** Cmdlet 會移除記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="939e5-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="939e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="939e5-107">EXAMPLES</span></span>

## <span data-ttu-id="939e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="939e5-108">PARAMETERS</span></span>

### <span data-ttu-id="939e5-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="939e5-109">-Name</span></span>
<span data-ttu-id="939e5-110">指定要移除的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="939e5-110">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="939e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939e5-111">-DefaultProfile</span></span>
<span data-ttu-id="939e5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="939e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="939e5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="939e5-113">-PassThru</span></span>
<span data-ttu-id="939e5-114">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="939e5-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="939e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939e5-115">CommonParameters</span></span>
<span data-ttu-id="939e5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="939e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939e5-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="939e5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939e5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="939e5-118">INPUTS</span></span>

## <span data-ttu-id="939e5-119">輸出</span><span class="sxs-lookup"><span data-stu-id="939e5-119">OUTPUTS</span></span>

### <span data-ttu-id="939e5-120">System.object</span><span class="sxs-lookup"><span data-stu-id="939e5-120">System.Boolean</span></span>

## <span data-ttu-id="939e5-121">筆記</span><span class="sxs-lookup"><span data-stu-id="939e5-121">NOTES</span></span>

## <span data-ttu-id="939e5-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="939e5-122">RELATED LINKS</span></span>

[<span data-ttu-id="939e5-123">附加 AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="939e5-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="939e5-124">AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="939e5-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


