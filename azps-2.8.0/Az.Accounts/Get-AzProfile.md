---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 937683c8592bb814b7f6a6262ef095cbd8252c78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614192"
---
# <span data-ttu-id="3758c-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="3758c-101">Get-AzProfile</span></span>

## <span data-ttu-id="3758c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3758c-102">SYNOPSIS</span></span>
<span data-ttu-id="3758c-103">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="3758c-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="3758c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3758c-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="3758c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3758c-105">DESCRIPTION</span></span>
<span data-ttu-id="3758c-106">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="3758c-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="3758c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3758c-107">EXAMPLES</span></span>

### <span data-ttu-id="3758c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3758c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="3758c-109">取得 KeyVault 模組支援的服務設定檔</span><span class="sxs-lookup"><span data-stu-id="3758c-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="3758c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3758c-110">PARAMETERS</span></span>

### <span data-ttu-id="3758c-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3758c-111">-ListAvailable</span></span>
<span data-ttu-id="3758c-112">列出已安裝模組支援的所有服務設定檔</span><span class="sxs-lookup"><span data-stu-id="3758c-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="3758c-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="3758c-113">-ModuleName</span></span>
<span data-ttu-id="3758c-114">要檢查的模組名稱</span><span class="sxs-lookup"><span data-stu-id="3758c-114">The name of the module to check</span></span>

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

### <span data-ttu-id="3758c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3758c-115">CommonParameters</span></span>
<span data-ttu-id="3758c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3758c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3758c-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3758c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3758c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="3758c-118">INPUTS</span></span>

### <span data-ttu-id="3758c-119">所有</span><span class="sxs-lookup"><span data-stu-id="3758c-119">None</span></span>

## <span data-ttu-id="3758c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="3758c-120">OUTPUTS</span></span>

### <span data-ttu-id="3758c-121">PSAzureServiceProfile 中的 CommonModule。</span><span class="sxs-lookup"><span data-stu-id="3758c-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="3758c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="3758c-122">NOTES</span></span>

## <span data-ttu-id="3758c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="3758c-123">RELATED LINKS</span></span>
