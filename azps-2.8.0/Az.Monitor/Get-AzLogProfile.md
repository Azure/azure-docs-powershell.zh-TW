---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 1f7306d78d7c0405929ba7dae2512b141a4f4a89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611792"
---
# <span data-ttu-id="3a9ac-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ac-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="3a9ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ac-103">取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-103">Gets a log profile.</span></span>

## <span data-ttu-id="3a9ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a9ac-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a9ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="3a9ac-105">DESCRIPTION</span></span>
<span data-ttu-id="3a9ac-106">**AzLogProfile** Cmdlet 會取得記錄設定檔。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="3a9ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="3a9ac-107">EXAMPLES</span></span>

## <span data-ttu-id="3a9ac-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a9ac-108">PARAMETERS</span></span>

### <span data-ttu-id="3a9ac-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ac-109">-DefaultProfile</span></span>
<span data-ttu-id="3a9ac-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3a9ac-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a9ac-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a9ac-111">-Name</span></span>
<span data-ttu-id="3a9ac-112">指定要取得的記錄設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ac-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ac-113">CommonParameters</span></span>
<span data-ttu-id="3a9ac-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ac-115">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ac-116">輸入</span><span class="sxs-lookup"><span data-stu-id="3a9ac-116">INPUTS</span></span>

### <span data-ttu-id="3a9ac-117">System.object</span><span class="sxs-lookup"><span data-stu-id="3a9ac-117">System.String</span></span>

## <span data-ttu-id="3a9ac-118">輸出</span><span class="sxs-lookup"><span data-stu-id="3a9ac-118">OUTPUTS</span></span>

### <span data-ttu-id="3a9ac-119">PSLogProfileCollection 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="3a9ac-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="3a9ac-120">筆記</span><span class="sxs-lookup"><span data-stu-id="3a9ac-120">NOTES</span></span>

## <span data-ttu-id="3a9ac-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a9ac-121">RELATED LINKS</span></span>

[<span data-ttu-id="3a9ac-122">附加 AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ac-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="3a9ac-123">移除-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ac-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


