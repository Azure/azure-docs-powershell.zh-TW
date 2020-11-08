---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129367"
---
# <span data-ttu-id="4c76f-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="4c76f-101">Get-AzProfile</span></span>

## <span data-ttu-id="4c76f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c76f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c76f-103">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c76f-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="4c76f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c76f-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="4c76f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c76f-105">DESCRIPTION</span></span>
<span data-ttu-id="4c76f-106">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="4c76f-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="4c76f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4c76f-107">EXAMPLES</span></span>

### <span data-ttu-id="4c76f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4c76f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="4c76f-109">取得 KeyVault 模組支援的服務設定檔</span><span class="sxs-lookup"><span data-stu-id="4c76f-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="4c76f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4c76f-110">PARAMETERS</span></span>

### <span data-ttu-id="4c76f-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="4c76f-111">-ListAvailable</span></span>
<span data-ttu-id="4c76f-112">列出已安裝模組支援的所有服務設定檔</span><span class="sxs-lookup"><span data-stu-id="4c76f-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="4c76f-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="4c76f-113">-ModuleName</span></span>
<span data-ttu-id="4c76f-114">要檢查的模組名稱</span><span class="sxs-lookup"><span data-stu-id="4c76f-114">The name of the module to check</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c76f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c76f-115">CommonParameters</span></span>
<span data-ttu-id="4c76f-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c76f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c76f-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c76f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c76f-118">輸入</span><span class="sxs-lookup"><span data-stu-id="4c76f-118">INPUTS</span></span>

### <span data-ttu-id="4c76f-119">所有</span><span class="sxs-lookup"><span data-stu-id="4c76f-119">None</span></span>

## <span data-ttu-id="4c76f-120">輸出</span><span class="sxs-lookup"><span data-stu-id="4c76f-120">OUTPUTS</span></span>

### <span data-ttu-id="4c76f-121">PSAzureServiceProfile 中的 CommonModule。</span><span class="sxs-lookup"><span data-stu-id="4c76f-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="4c76f-122">筆記</span><span class="sxs-lookup"><span data-stu-id="4c76f-122">NOTES</span></span>

## <span data-ttu-id="4c76f-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c76f-123">RELATED LINKS</span></span>
