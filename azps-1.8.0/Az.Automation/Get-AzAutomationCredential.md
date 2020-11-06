---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623082"
---
# <span data-ttu-id="22781-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22781-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="22781-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22781-102">SYNOPSIS</span></span>
<span data-ttu-id="22781-103">取得自動化認證。</span><span class="sxs-lookup"><span data-stu-id="22781-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="22781-104">句法</span><span class="sxs-lookup"><span data-stu-id="22781-104">SYNTAX</span></span>

### <span data-ttu-id="22781-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="22781-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22781-106">ByName</span><span class="sxs-lookup"><span data-stu-id="22781-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22781-107">說明</span><span class="sxs-lookup"><span data-stu-id="22781-107">DESCRIPTION</span></span>
<span data-ttu-id="22781-108">**AzAutomationCredential** Cmdlet 會取得一或多個 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="22781-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="22781-109">根據預設，會傳回所有認證。</span><span class="sxs-lookup"><span data-stu-id="22781-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="22781-110">指定認證的名稱以取得特定認證。</span><span class="sxs-lookup"><span data-stu-id="22781-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="22781-111">為安全起見，這個 Cmdlet 不會傳回認證密碼。</span><span class="sxs-lookup"><span data-stu-id="22781-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="22781-112">示例</span><span class="sxs-lookup"><span data-stu-id="22781-112">EXAMPLES</span></span>

### <span data-ttu-id="22781-113">範例1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="22781-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="22781-114">這個命令會針對自動化帳戶（名為 Contoso17）中的所有認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="22781-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="22781-115">範例2：取得認證</span><span class="sxs-lookup"><span data-stu-id="22781-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="22781-116">這個命令會在名為 Contoso17 的自動化帳戶中，為名為 ContosoCredential 的認證取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="22781-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="22781-117">參數</span><span class="sxs-lookup"><span data-stu-id="22781-117">PARAMETERS</span></span>

### <span data-ttu-id="22781-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22781-118">-AutomationAccountName</span></span>
<span data-ttu-id="22781-119">指定此 Cmdlet 為其檢索認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="22781-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22781-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22781-120">-DefaultProfile</span></span>
<span data-ttu-id="22781-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="22781-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22781-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="22781-122">-Name</span></span>
<span data-ttu-id="22781-123">指定要取得認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="22781-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22781-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22781-124">-ResourceGroupName</span></span>
<span data-ttu-id="22781-125">指定此 Cmdlet 為其檢索認證的資源群組。</span><span class="sxs-lookup"><span data-stu-id="22781-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22781-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22781-126">CommonParameters</span></span>
<span data-ttu-id="22781-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22781-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22781-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22781-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22781-129">輸入</span><span class="sxs-lookup"><span data-stu-id="22781-129">INPUTS</span></span>

### <span data-ttu-id="22781-130">System.object</span><span class="sxs-lookup"><span data-stu-id="22781-130">System.String</span></span>

## <span data-ttu-id="22781-131">輸出</span><span class="sxs-lookup"><span data-stu-id="22781-131">OUTPUTS</span></span>

### <span data-ttu-id="22781-132">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="22781-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="22781-133">筆記</span><span class="sxs-lookup"><span data-stu-id="22781-133">NOTES</span></span>

## <span data-ttu-id="22781-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="22781-134">RELATED LINKS</span></span>

[<span data-ttu-id="22781-135">新-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22781-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="22781-136">移除-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22781-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="22781-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="22781-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


