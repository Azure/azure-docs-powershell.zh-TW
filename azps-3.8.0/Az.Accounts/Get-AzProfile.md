---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzProfile.md
ms.openlocfilehash: 165a85f48bc39608bd636073b4b12427e0a81bf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958957"
---
# <span data-ttu-id="f5082-101">Get-AzProfile</span><span class="sxs-lookup"><span data-stu-id="f5082-101">Get-AzProfile</span></span>

## <span data-ttu-id="f5082-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5082-102">SYNOPSIS</span></span>
<span data-ttu-id="f5082-103">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="f5082-103">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f5082-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5082-104">SYNTAX</span></span>

```
Get-AzProfile [-ModuleName <String[]>] [-ListAvailable] [<CommonParameters>]
```

## <span data-ttu-id="f5082-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5082-105">DESCRIPTION</span></span>
<span data-ttu-id="f5082-106">取得已安裝的模組支援的服務設定檔。</span><span class="sxs-lookup"><span data-stu-id="f5082-106">Get the service profiles supported by installed modules.</span></span>

## <span data-ttu-id="f5082-107">示例</span><span class="sxs-lookup"><span data-stu-id="f5082-107">EXAMPLES</span></span>

### <span data-ttu-id="f5082-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f5082-108">Example 1</span></span>
```powershell
PS C:\> Get-AzProfile -ModuleName Az.KeyVault

Name              Description
----              -----------
latest-2019-04-30 A snapshot of the service API versions in the Azure Global Cloud. This profile was defined in April 2019.
hybrid-2019-03-01 A snapshot of the Service API versions in AzureStack, Azure Sovereign clouds, and the Azure Global Cloud. This profile was defined                    in March 2019.
```

<span data-ttu-id="f5082-109">取得 KeyVault 模組支援的服務設定檔</span><span class="sxs-lookup"><span data-stu-id="f5082-109">Get the service profile supported by the KeyVault module</span></span>

## <span data-ttu-id="f5082-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5082-110">PARAMETERS</span></span>

### <span data-ttu-id="f5082-111">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f5082-111">-ListAvailable</span></span>
<span data-ttu-id="f5082-112">列出已安裝模組支援的所有服務設定檔</span><span class="sxs-lookup"><span data-stu-id="f5082-112">List all service profiles supported by installed modules</span></span>

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

### <span data-ttu-id="f5082-113">-ModuleName</span><span class="sxs-lookup"><span data-stu-id="f5082-113">-ModuleName</span></span>
<span data-ttu-id="f5082-114">要檢查的模組名稱</span><span class="sxs-lookup"><span data-stu-id="f5082-114">The name of the module to check</span></span>

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

### <span data-ttu-id="f5082-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5082-115">CommonParameters</span></span>
<span data-ttu-id="f5082-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5082-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5082-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5082-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5082-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f5082-118">INPUTS</span></span>

### <span data-ttu-id="f5082-119">所有</span><span class="sxs-lookup"><span data-stu-id="f5082-119">None</span></span>

## <span data-ttu-id="f5082-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f5082-120">OUTPUTS</span></span>

### <span data-ttu-id="f5082-121">PSAzureServiceProfile 中的 CommonModule。</span><span class="sxs-lookup"><span data-stu-id="f5082-121">Microsoft.Azure.Commands.Profile.CommonModule.PSAzureServiceProfile</span></span>

## <span data-ttu-id="f5082-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f5082-122">NOTES</span></span>

## <span data-ttu-id="f5082-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5082-123">RELATED LINKS</span></span>
