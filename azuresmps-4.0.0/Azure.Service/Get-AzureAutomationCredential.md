---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967105"
---
# <span data-ttu-id="8b63f-101">Get-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b63f-101">Get-AzureAutomationCredential</span></span>

## <span data-ttu-id="8b63f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b63f-102">SYNOPSIS</span></span>

<span data-ttu-id="8b63f-103">取得 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="8b63f-103">Gets an Azure Automation credential.</span></span>

## <span data-ttu-id="8b63f-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b63f-104">SYNTAX</span></span>

### <span data-ttu-id="8b63f-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="8b63f-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8b63f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8b63f-106">ByName</span></span>
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b63f-107">說明</span><span class="sxs-lookup"><span data-stu-id="8b63f-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8b63f-108">**AzureAutomationCredential** Cmdlet 會取得一或多個 Microsoft Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="8b63f-108">The **Get-AzureAutomationCredential** cmdlet gets one or more Microsoft Azure Automation credentials.</span></span>
<span data-ttu-id="8b63f-109">根據預設，會傳回所有認證。</span><span class="sxs-lookup"><span data-stu-id="8b63f-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="8b63f-110">若要取得特定認證，請指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="8b63f-110">To get a specific credential, specify its name.</span></span>

## <span data-ttu-id="8b63f-111">示例</span><span class="sxs-lookup"><span data-stu-id="8b63f-111">EXAMPLES</span></span>

### <span data-ttu-id="8b63f-112">範例1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="8b63f-112">Example 1: Get all credentials</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8b63f-113">這個命令會取得自動帳戶（名為 Contoso17）中的所有認證。</span><span class="sxs-lookup"><span data-stu-id="8b63f-113">This command gets all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8b63f-114">範例2：取得認證</span><span class="sxs-lookup"><span data-stu-id="8b63f-114">Example 2: Get a credential</span></span>
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

<span data-ttu-id="8b63f-115">這個命令會取得名為 MyCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="8b63f-115">This command gets the credential named MyCredential.</span></span>

## <span data-ttu-id="8b63f-116">參數</span><span class="sxs-lookup"><span data-stu-id="8b63f-116">PARAMETERS</span></span>

### <span data-ttu-id="8b63f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b63f-117">-AutomationAccountName</span></span>
<span data-ttu-id="8b63f-118">指定要取得認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8b63f-118">Specifies the name of the automation account with the credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b63f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b63f-119">-Name</span></span>
<span data-ttu-id="8b63f-120">指定要取得認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b63f-120">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b63f-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8b63f-121">-Profile</span></span>
<span data-ttu-id="8b63f-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8b63f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8b63f-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8b63f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b63f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b63f-124">CommonParameters</span></span>
<span data-ttu-id="8b63f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b63f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b63f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b63f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b63f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8b63f-127">INPUTS</span></span>

## <span data-ttu-id="8b63f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8b63f-128">OUTPUTS</span></span>

### <span data-ttu-id="8b63f-129">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b63f-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="8b63f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8b63f-130">NOTES</span></span>

## <span data-ttu-id="8b63f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b63f-131">RELATED LINKS</span></span>

[<span data-ttu-id="8b63f-132">新-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b63f-132">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="8b63f-133">移除-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b63f-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="8b63f-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8b63f-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


